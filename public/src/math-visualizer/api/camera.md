# Camera

## Описание

Класс, который позволяет управлять положением и ориентацией камеры в пространстве.

## Публичные поля

<code class="language-C++">float movementSpeed</code> – скорость передвижения камеры, при вызове
методов <code class="language-C++">move()</code>.

## Методы и конструкторы

<code class="language-C++"> Camera(const glm::vec3 position, const glm::vec3 camera_up, const float camera_yaw, const float camera_pitch)
</code> – конструктор, который инициализирует положение и ориентацию камеры.

<code class="language-C++">glm::mat4 getViewMatrix() const</code> – возвращает матрицу вида камеры.

<code class="language-C++">float getZoom() const noexcept</code> – возвращает угол обзора камеры.

<code class="language-C++">void move(const CameraMovement direction, const float deltaTime)</code> – перемещает камеру в заданном направлении.

<code class="language-C++">void rotate(const double x_pos_in, const double y_pos_in)</code> – поворачивает камеру по оси X и Y .

<code class="language-C++">void processMouseMovement(float xOffset, float yOffset, const GLboolean constrainPitch)</code> – обрабатывает движение мыши.

<code class="language-C++">void processMouseScroll(float yOffset)</code> – обрабатывает прокрутку колеса мыши, изменяя zoom.

<code class="language-C++">void move(const float delta_time, const float multiplier = 1.0F)</code> – перемещает камеру вперед, назад, влево, вправо, в зависимости от вызванной функции.

