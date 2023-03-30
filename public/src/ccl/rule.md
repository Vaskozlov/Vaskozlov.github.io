# Правило для лексического анализатора

Модификаторы правила:
- ! - элемент может стоять в любом месте (рекомендуется применять к терминальным символам грамматики)

Правило состоит из 4 основных элементов:
- [множества символов](union.md)
- [строчки](sequence.md)
- [логического элемента](logical.md)
- [контейнера правил](crate.md)

К каждому правилу могут быть применены следующие постфиксальные модификаторы:
- p - элемент является префиксом/постфиксом (изначально создается префикс, но если уже существует элемент, который не является префиксным, то создается постфикс)
- ^ - все, кроме данного элемента
- {n, m} - элемент повторяется от n до m раз включительно
- \* - повторяется ноль раз или больше
- \+ - повторяется больше нулю раз
- \? - повторяется 0 или 1 раз

Примеры правил можно найти [тут](examples.md)