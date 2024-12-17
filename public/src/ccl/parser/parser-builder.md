# ParserBuilder

Класс `ParserBuilder` хранит в себе созданные правила и позволяет сгенерировать различные типы парсеров по ним.

## Методы и конструктор

<code class="language-C++">ParserBuilder(const std::unordered_map<std::string, SmallId> &default_rules)</code> –
принимает на вход словарь с правилами по умолчанию (более подробно про словарь с правилами написано в [RulesReader](rules-reader.md).

<code class="language-C++">LrParser buildLr1()</code> – создает LR(1) парсер.

<code class="language-C++">GlrParser buildGlr()</code> – создает GLR парсер.

<code class="language-C++">Ll1Parser buildLl1()</code> – создает LL(1) парсер.

<code class="language-C++">GllParser buildGLL()</code> – создает GLL парсер.

<code class="language-C++">SmallId addRule(const std::string &rule_name)</code> – добавляет правило в генератор парсеров и возвращает уникальный номер созданного правила.

<code class="language-C++">std::function<std::string(SmallId)> getIdToNameTranslationFunction() const</code> – создает функцию, которая по уникальному номеру возвращает название правила.

