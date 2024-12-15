# PolygonShape
## Описание
Базовый класс объекта сцены. Содержит в себе информацию, о вершинах фигуры и определяет методы для работы с ней.

## Объявление
```C++
class Shape : public VerticesContainer<glm::vec3>
```

## Методы и конструкторы
<code class="language-C++">Shape()</code>

<code class="language-C++">virtual ~Shape()</code>

<code class="language-C++">void draw() const</code> – устанавливает VAO фигуры и вызывает метод doDraw.

<code class="language-C++">virtual void doDraw() const = 0</code> – реализует отрисовку фигуры.

<code class="language-C++">void drawAt(const Shader &shader, const glm::vec3 location, const float angle = 0.0F, const glm::vec3 rotation_vec) const </code> – отрисовывает фигуру с заданным смещением и углом поворота.