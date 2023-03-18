# Общие математические функции

В fsc есть ряд встроенные функций для выполнения математических операций и все они могут быть исполнены во время сборки.

- <code class="language-Swift">sqrt(in float x) -> float</code> - вычисляет квадратный корень
- <code class="language-Swift">log2(in float x) -> float</code> - логарифм по основанию 2 данного числа
- <code class="language-Swift">log10(in float x) -> float</code> - логарифм по основанию 10 данного числа
- <code class="language-Swift">log(in float x) -> float</code> - вычисляет натуральный логарифм
- <code class="language-Swift">log(in float x, in float base) -> float</code> - логарифм данного числа по данному основанию
- <code class="language-Swift">trunc(in float x) -> float</code> - ближайшее целое число, не превышающее по величине заданное значение 
- <code class="language-Swift">floor(in float x) -> float</code> - ближайшее целое число не больше заданного значения 
- <code class="language-Swift">ceil(in float x) -> float</code> - ближайшее целое число не меньшее заданного значения 
- <code class="language-Swift">round(in float x) -> float</code> - ближайшее целое число, округление от нуля в промежуточных случаях
- <code class="language-Swift">abs(in any_numeric x) -> float</code> - вычисляет абсолютное значение целого числа
- <code class="language-Swift">sin(in float x) -> float</code> - вычисляет синус
- <code class="language-Swift">cos(in float x) -> float</code> - вычисляет косинус
- <code class="language-Swift">tan(in float x) -> float</code> - вычисляет тангенс
- <code class="language-Swift">asin(in float x) -> float</code> - вычисляет арксинус
- <code class="language-Swift">acos(in any_numeric x) -> float</code> - вычисляет арккосинус 
- <code class="language-Swift">atan(in any_numeric x) -> float</code> - вычисляет арктангенс
- <code class="language-Swift">atan2(in any_numeric y, in any_numeric x) -> float</code> - арктангенс, используя знаки для определения квадрантов
