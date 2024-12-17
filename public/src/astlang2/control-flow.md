## Control flow
- `if` - условный оператор
    - `elif` - ветвь условного оператора
    - `else` - ветвь условного оператора
- `while` - цикл с предусловием

```astlang2
var i = 0;

while i < 10 {
    println(i);
    i = i + 1;
}

println("Done!");
```
Вывод программы:
```
0
1
2
3
4
5
6
7
8
9
Done!
```

```astlang2
var a = 5;

if a > 3 {
    println("a is greater than 3");
} elif a == 3 {
    println("a is equal to 3");
} else {
    println("a is less than 3");
}
```
Вывод программы:
```
a is greater than 3
```
