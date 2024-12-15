# Базовый класс приложения

## Описание
Базовый класс OpenGl приложение с интеграцией ImGUI.

## Методы класса
<code class="language-C++">Application(int width, int height, std::string window_title, int multisampling_level = 4)</code> – создает окно приложения с заданными параметрами и производит инициализацию OpenGL, GLFW, ImGUI.

<code class="language-C++">virtual ~Application()</code>

<code class="language-C++">void run()</code> – запускает цикл обработки событий и отрисовки.

<code class="language-C++">virtual void init()</code> – метод инициализации приложения.

<code class="language-C++">virtual void update()</code> – метод обновления приложения.

<code class="language-C++">virtual void onResize(int width, int height)</code> – вызывается при изменении размера приложения.

<code class="language-C++">virtual void onMouseMovement(double x_pos_in, double y_pos_in)</code> – вызывается при движении мыши, в качестве параметром передается позиция мыши.

<code class="language-C++">virtual void onMouseRelativeMovement(double delta_x, double delta_y)</code> – вызывается при движении мыши, в качестве параметров передается относительное передвижение мыши (от прошлого кадра).

<code class="language-C++">virtual void onScoll(double x_offset, double y_offset)</code> – вызывается при прокрутке колеса мыши.

<code class="language-C++">void setClearColor(glm::vec4 clear_color)</code> – устанавливает цвет очистки экрана.

<code class="language-C++">virtual void processInput()</code> – вызывается при вводе изменении состояния ввода с клавиатуры.

<code class="language-C++">virtual void onLeaveOrEnter(bool entered)</code> – вызывается при выходе приложения из фокуса пользователя и при появлении в фокусе.

<code class="language-C++">template<b::embed_string_literal fontPath> \
ImFont * loadFont(const float font_size = 45.0F) const</code> – загружает шрифт для ImGui из встроенного ресурса.

