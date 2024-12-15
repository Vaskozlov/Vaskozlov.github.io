# Sphere
## Описание 
Класс для создания сферы. В результате будет создан PolygonsShape, который можно добавить в сцену.

## Объявление
```C++
class Sphere final : public detail::PolygonsShape
```

## Методы и конструкторы
<code class="language-C++">Sphere(float radius, isl::u32 slices, isl::u32 stacks)</code> – создает сферу с заданным радиусом и количеством фрагментов.

