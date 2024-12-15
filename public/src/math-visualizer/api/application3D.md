# Базовый класс приложения для 3D графики

## Описание
Базовый класс OpenGl приложение для 3D графики с интеграцией ImGUI.

## Объявление
```cpp
class Application3D : public Application
```

## Методы класса
<code class="language-C++">void processInput() override</code> – вызывает метод базового класса и изменяет позицию камеры, по нажатию клавиш W, A, S, D.

