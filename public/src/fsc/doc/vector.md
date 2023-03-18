# Динамический массив: Vector\<T\>

## Объявление

Динамический массив имеет имя <code class="language-Swift">Vector\<T\></code>.

 - <code class="language-Swift">Vector\<T\>()</code>
 - <code class="language-Swift">Vector\<T\>(T, T...)</code>

## Методы

- <code class="language-Swift">size() -> u64</code> - возвращает длину массива
- <code class="language-Swift">at(in u64 index) -> T</code> - возвращает элемент массива по заданному индексу
- <code class="language-Swift">max() -> T</code> - возвращает максимальный элемент в массиве
- <code class="language-Swift">min() -> T</code> - возвращает минимальный элемент в массиве
- <code class="language-Swift">max(in T default) -> T</code> - если массив пустой, то возвращает `default`, иначе максимальное значение в массиве
- <code class="language-Swift">min(in T default) -> T</code> - если массив пустой, то возвращает `default`, иначе минимальный значение в массиве
- <code class="language-Swift">push_back(in T value) -> void</code> - добавляет элемент в конец массива
- <code class="language-Swift">swap(in u64 first, in u64 second) -> void</code> - переставляет элементы по индексу 'first' и 'second' местами

## Перезагруженные операторы

- <code class="language-Swift">\_\_at\_\_(in u64 index) -> T</code> - поведение аналогично методы at