# VBO
## Описание 
VAO (Vertex Array Object) - это объект, который хранит настройки вершинных атрибутов. VAO используется для хранения настроек вершинных атрибутов, таких как позиция, цвет, текстурные координаты и т.д.

## Методы и конструкторы
<code class="language-C++">VAO()</code> - создает VAO, сохраняя его номер в переменной instanceVAO.

<code class="language-C++">~VAO()</code> - удаляет созданный объект.

<code class="language-C++">void bind() const</code> – привязывает VAO к текущему контексту OpenGL.

<code class="language-C++">void unbind() const</code> - отвязывает VAO от текущего контекста OpenGL.

<code class="language-C++">void bind(GLsizei array_attribute, GLint size, GLenum type, GLsizei stride, GLsizei offset)</code> - устанавливает атрибуты вершинного массива для шейдера.

<code class="language-C++">void bindInstanceParameters(GLsizei array_attribute, GLint divisor)</code> - устанавливает параметры инстансирования для шейдера.


