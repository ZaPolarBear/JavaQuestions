String является [ссылочным](Ссылочные) типом данных для работы со строками данных

Пример инициализации:
String str = "Hello" - Cоздание строки с использованием литерала
String str = new String("Hello") - Cоздание с помощью оператора new 

Строки в java неизменяемы:
String str = "Hello";
str = str + " World"; - Создается новая строка "Hello World", а не изменяется существующая строка

Сравнение строк: 
Для сравнения строк в Java используются методы equals() и compareTo(). Метод equals() сравнивает содержимое строк, в то время как метод compareTo() сравнивает лексикографические значения строк. Например:
String str1 = "Hello";
String str2 = "World";
boolean isEqual = str1.equals(str2); - Сравнение содержимого строк (false)
int result = str1.compareTo(str2); - Сравнение лексикографических значений (-15)

Так же для работы со строками в Java есть следующие типы данных:
[[StringBuffer]]
[[StringBuilder]]
[[CharSequence]]

[[Пул строк]]
