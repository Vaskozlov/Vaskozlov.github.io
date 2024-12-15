# VBO
## Описание 
VBO (Vertex Buffer Object) - это объект, который хранит массив вершинных данных. VBO используется для хранения вершинных данных, таких как позиция, цвет, текстурные координаты и т.д.

## Методы и конструкторы
<code class="language-C++">VBO()</code> - создает VBO, сохраняя его номер в переменной instanceVBO.

<code class="language-C++">~VBO()</code> - удаляет созданный буфер.

<code class="language-C++">void bind() const</code> - привязывает VBO к текущему контексту OpenGL.

<code class="language-C++">void unbind() const</code> - отвязывает VBO от текущего контекста OpenGL.

<code class="language-C++">void setData(const void *data, size_t size, GLenum mode = GL_STATIC_DRAW)</code> - загружает данные в VBO по переделанному адресу.

