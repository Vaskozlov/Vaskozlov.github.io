# Оператор if-elif-else

Сначала записывается часть <code class="language-Swift">if</code> с условным выражением, далее могут следовать одна или более необязательных частей <code class="language-Swift">elif</code>, и, наконец, необязательная часть  <code class="language-Swift">else</code>.

```Swift
if условие {
    инструкции
}
```

Условие должно являться логическим значением.

```Swift
if x == 10 {
    print(10)
}
```

```Swift
if x > 10 {
    print("x is greater than 10")
}
elif x < 10 {
    print("x is less than 0")
}
else {
    print("x is in [0, 10])
}
```
