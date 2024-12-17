# RulesReader

Класс `RulesReader` предназначен для чтения правил из файла и создания генератора парсеров.

## Методы и конструктор
<code class="language-C++">RulesReader(
const std::unordered_map<std::string, SmallId> &default_rules,
isl::string_view input, isl::string_view filename = {})</code> – принимает на вход словарь с правилами по умолчанию, строку с текстом правил и имя файла, из которого был прочитан текст. Ключом в словаре правил по умолчанию служит название правила, а значение это уникальный номер правила.

<code class="language-C++">ParserBuilder & getParserBuilder()</code> – возвращает генератор парсеров.
