# Строчка FSC

## Объявление

Строка имеет имя <code class="language-Swift">String\<T\></code> и содержит символы [UTF-8](https://ru.wikipedia.org/wiki/UTF-8).


Строку может задать при помощи символов, заключенных между " или явным конструированием типа: <br />
- <code class="language-Swift">"Hello, World!"</code> <br />
- <code class="language-Swift">String("\u0xDADA")</code>


## Методы

- <code class="language-Swift">size() -> u64</code> - возвращает количество символов 
- <code class="language-Swift">toI32() -> i32</code> - преобразует строку в целое число i32
- <code class="language-Swift">toI64() -> i64</code> - преобразует строку в целое число i64
- <code class="language-Swift">toU64() -> u64</code> - преобразует строку в целое число u64
- <code class="language-Swift">toF32() -> f32</code> - преобразует строку значение с плавающей запятой число f32
- <code class="language-Swift">toF64() -> f64</code> - преобразует строку значение с плавающей запятой число f64
- <code class="language-Swift">at(in u64 index) -> char</code> - обращается к указанному символу с проверкой границ 

## Перезагруженные операторы

- <code class="language-Swift">\_\_at\_\_(in u64 index) -> char</code> - поведение аналогично методу at
- <code class="language-Swift">\_\_add\_\_(in String lhs, in String rhs) -> String</code> - объединяет две строки
- <code class="language-Swift">\_\_mul\_\_(in String str, in u64 times) -> String</code> - повторяет строку заданное число раз