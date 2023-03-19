# Динамический массив: Vector\<T\>

## Объявление
 - <code class="language-Swift">Vector\<T\>()</code>
 - <code class="language-Swift">Vector\<T\>(T, T...)</code>

## Методы

- <code class="language-Swift">size() -> u64</code> - возвращает количество элементов 
- <code class="language-Swift">at(in u64 index) -> T</code> - обращается к указанному элементу с проверкой границ 
- <code class="language-Swift">max() -> T</code> - возвращает наибольший элемент
- <code class="language-Swift">min() -> T</code> - возвращает наименьший элемент
- <code class="language-Swift">max(in T default) -> T</code> - если массив пустой, то возвращает `default`, иначе наибольший элемент
- <code class="language-Swift">min(in T default) -> T</code> - если массив пустой, то возвращает `default`, наименьший элемент
- <code class="language-Swift">sort(in bool reverse = false) -> void</code> - сортирует массив
- <code class="language-Swift">swap(in u64 first, in u64 second) -> void</code> - обмен элементов по первому и второму переданному индексу
- <code class="language-Swift">push_back(in T value) -> void</code> - добавляет элемент в конец
- <code class="language-Swift">pop_back() -> void</code> - удаляет последний элемент 

## Перезагруженные операторы

- <code class="language-Swift">\_\_at\_\_(in u64 index) -> T</code> - поведение аналогично методу at