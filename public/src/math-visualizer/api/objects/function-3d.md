# Function3D
## Описание 
Класс для создания функции в 3D. В результате будет создан PolygonsShape, который можно добавить в сцену.

## Объявление
```C++
class Function3D final : public detail::PolygonsShape
```

## Методы и конструкторы
<code class="language-C++">Function3D(const std::function<float(glm::vec2)> &function, const float min_x, const float min_y,
const float min_z, const float max_x, const float max_y, const float max_z)</code> – создает функцию по заданной формуле.

