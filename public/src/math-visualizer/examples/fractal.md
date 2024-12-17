# Фрактал

<video controls>
  <source src="../../images/mandelbrot.mov" type="video/mp4">
</video>

```C++
class FractalApplication final : public mv::Application2D
{
private:
    std::array<char, 128> imguiWindowBuffer{};

    mv::Shader mandelbrotFractalShader = mv::Shader{
        {b::embed<"resources/shaders/fractal/default.vert">().str()},
        {
            b::embed<"resources/shaders/fractal/mandelbrot.frag">().str(),
            b::embed<"resources/shaders/fractal/common.glsl">().str(),
        },
    };

    // Поле где будет рисоваться фрактал
    mv::gl::VerticesContainer<glm::vec3> mandelbrotVertices{
        {2.0F, 2.0F, 0.0F}, {2.0F, -2.0F, 0.0F},  {-2.0F, -2.0F, 0.0F},
        {2.0F, 2.0F, 0.0F}, {-2.0F, -2.0F, 0.0F}, {-2.0F, 2.0F, 0.0F},
    };

    double pressTime = 0.0;
    ImFont *font = nullptr;
    float fontScale = 0.5F;
    int mandelbrotIterations = 1000;

public:
    using Application2D::Application2D;

    auto init() -> void override
    {
        Application2D::init();
        glfwSetInputMode(window, GLFW_CURSOR, GLFW_CURSOR_DISABLED);

        mandelbrotVertices.loadData();
        mandelbrotVertices.vbo.bind();
        mandelbrotVertices.vao.bind(0, 3, GL_FLOAT, sizeof(glm::vec3), 0);

        // снижаем чувствительность камеры
        camera.movementSpeed = 0.5F;

        ImGui::StyleColorsDark();
        font = loadFont<"resources/fonts/JetBrainsMono-Medium.ttf">(30.0F);

        mandelbrotFractalShader.use();
        mandelbrotFractalShader.setInt("iterations", mandelbrotIterations);
    }

    auto mandelbrotFractal() -> void
    {
        if (ImGui::SliderInt("Iterataions", &mandelbrotIterations, 5, 4000)) {
            mandelbrotFractalShader.use();
            mandelbrotFractalShader.setInt("iterations", mandelbrotIterations);
        }

        mandelbrotFractalShader.use();
        mandelbrotFractalShader.setMat4("projection", getResultedViewMatrix());
        mandelbrotVertices.vao.bind();

        glDrawArrays(GL_TRIANGLES, 0, mandelbrotVertices.vertices.size());
    }

    auto update() -> void override
    {
        fmt::format_to_n(
            imguiWindowBuffer.data(), imguiWindowBuffer.size(),
            "Настройки. FPS: {:#.4}###SettingWindowTitle", ImGui::GetIO().Framerate);

        ImGui::Begin(imguiWindowBuffer.data());
        ImGui::PushFont(font);
        ImGui::SetWindowFontScale(fontScale);

        mandelbrotFractal();

        if (ImGui::Button("Center camera")) {
            camera.setPosition(glm::vec3(0.0F, 0.0F, 2.0F));
        }

        ImGui::SameLine();

        ImGui::SliderFloat("Font scale", &fontScale, 0.1F, 1.5F, "%.3f");

        ImGui::PopFont();
        ImGui::End();
    }

    auto processInput() -> void override
    {
        constexpr static auto key_press_delay = 0.2;

        Application2D::processInput();

        const auto left_alt_pressed = glfwGetKey(window, GLFW_KEY_LEFT_ALT) == GLFW_PRESS;
        const auto key_g_pressed = glfwGetKey(window, GLFW_KEY_G) == GLFW_PRESS;

        if (left_alt_pressed && key_g_pressed) {
            const auto mode = glfwGetInputMode(window, GLFW_CURSOR);
            const double new_press_time = glfwGetTime();

            if (new_press_time - pressTime < key_press_delay) {
                return;
            }

            pressTime = new_press_time;
            firstMouse = true;
            isMouseShowed = mode == GLFW_CURSOR_DISABLED;

            glfwSetInputMode(
                window, GLFW_CURSOR, isMouseShowed ? GLFW_CURSOR_NORMAL : GLFW_CURSOR_DISABLED);
        }
    }

    // Перемещаем камеру относительно мыши
    auto onMouseRelativeMovement(const double delta_x, const double delta_y) -> void override
    {
        const auto scale = camera.getZoom() / 9000.0F;

        camera.relativeMove(camera.getUp() * static_cast<float>(delta_y) * scale);
        camera.relativeMove(camera.getRight() * static_cast<float>(delta_x) * scale);
    }
    
    // Масштабируем скорость зума в зависимости от приближения
    auto onScroll(const double x_offset, const double y_offset) -> void override
    {
        const auto scale = static_cast<double>(camera.getZoom()) / 90.0;
        Application2D::onScroll(x_offset * scale, y_offset * scale);
    }
};
```

