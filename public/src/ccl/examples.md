# Примеры правил

- ```! [+]``` - знак сложения, который может находиться где угодно
- ```[0-9]+ ( [a-zA-Z_] [a-zA-Z0-9_]* )?p``` - последовательность цифр, за которой следует опциональный постфикс в виде идентификатора
- ```! "\"" (["\n]^ | "\\\"")* "\""``` - элемент, который заключен между " и может находиться в любом месте; внутри него находятся либо символы, кроме " и символа новой строки, либо \\" (стандартная строчка в языке программирования)