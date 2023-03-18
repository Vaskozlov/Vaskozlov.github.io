# Структура программы на языке FSC

Программа может состоять из [функций](function.md), [классов](class.md) и [глобальных переменных](variable.md).<br />
По умолчанию выполнение начинается с функции main.

Пример программы:

```Swift
class S
{
    public var someVariable : i32

    public func __init__()
    {
        someVariable = 42
    }
}

var foo = S().someVariable

func main()
{
    print("{}\n", foo)
    return 0
}
```

```
> 42
```
