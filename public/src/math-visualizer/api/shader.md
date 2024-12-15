# Shader
## Описание
Класс Shader, предназначен для создания шейдера. Класс собирает шейдер из исходного кода и компилирует его. Поддерживаются шейдеры типа вершинный и фрагментный. После компиляции содержит в себе номер программы, после вызова деструктора программа будет уничтожена.

## Методы и конструкторы

<code class="language-C++">Shader(  const std::vector\<std::string\> &vertex_shaders,
const std::vector\<std::string\> &fragment_shaders)</code> – в качестве аргументов передаются исходные коды шейдеров на языке GLSL.

<code class="language-C++">~Shader()</code> – деструктор.

<code class="language-C++">void use()</code> – активирует шейдер.

<code class="language-C++">void setBool(const std::string &name, bool value) const</code> – устанавливает значение типа bool в uniform шейдера.

<code class="language-C++">void setInt(const std::string &name, int value) const</code> – устанавливает значение типа int в uniform шейдера.

<code class="language-C++">void setFloat(const std::string &name, float value) const</code> – устанавливает значение типа float в uniform шейдера.

<code class="language-C++">void setVec2(const std::string &name, const glm::vec2 &value) const</code> – устанавливает значение типа glm::vec2 в uniform шейдера.

<code class="language-C++">void setVec3(const std::string &name, const glm::vec3 &value) const</code> – устанавливает значение типа glm::vec3 в uniform шейдера.

<code class="language-C++">void setVec4(const std::string &name, const glm::vec4 &value) const</code> – устанавливает значение типа glm::vec4 в uniform шейдера.

<code class="language-C++">void setMat2(const std::string &name, const glm::mat2 &mat) const</code> – устанавливает значение типа glm::mat2 в uniform шейдера.

<code class="language-C++">void setMat3(const std::string &name, const glm::mat3 &mat) const</code> – устанавливает значение типа glm::mat3 в uniform шейдера.

<code class="language-C++">void setMat4(const std::string &name, const glm::mat4 &mat) const</code> – устанавливает значение типа glm::mat4 в uniform шейдера.