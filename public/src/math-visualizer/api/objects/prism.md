# Prism
## Описание 
Класс для создания призмы. В результате будет создан Polygon, который можно добавить в сцену.

## Объявление
```C++
class Prism : public detail::Polygon
```

## Методы и конструкторы
<code class="language-C++">Prism(float radius, float height, uint32_t vertices_count)</code> – создает призму заданной высоты и с основанием, равным правильному многоугольнику с радиусом описанной окружности равным radius.
