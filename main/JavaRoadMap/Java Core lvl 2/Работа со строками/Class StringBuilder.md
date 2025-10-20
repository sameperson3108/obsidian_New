StringBuilder (Изменяемые строки, НЕ потокобезопасные)

- Изменяемый - можно менять содержимое
- Быстрый для операций модификатор
- НЕ потокобезопасный
- Рекомендуется для одно поточных приложений

StringBuilder sb1 = new StringBuilder(); // ёмкость 16 по умолчанию
StringBuilder sb2 = new StringBuilder(50); // с указанием начальной ёмкости
StringBuilder sb3 = new StringBuilder("Album") // из строки



StringBuilder sb = new StringBuilder("Hello");

sb.append(" ").append("World") - добавление
System.out.println(sb); // Hello World

sb.insert(6, "Java ") - вставка, число - индекс куда вставлять
System.out.println(sb); // Hello Java World

sb.replcae(6, 10, "Python") - замена, числа - с какого по какой индекс
System.out.println(sb); // Hello Python World

sb.delete(6, 13) - удаление, с какого по какой индекс
System.out.println(sb); // Hello World

sb.reverse() - переворот строки
System.out.println(sb); // dlroW olleH

sb.setLength(5) - установка длины
System.out.println(sb); // Hello

sb.setCharAt(1, 'a') - замена символа под индексом
System.out.println(sb); // Hallo

sb.length() - длина
sb.capacity() - ёмкость

String str = sb.toString() - преобразование в String


Использование:
- Для построения сложных строк в одном потоке
- Динамическое построение запроса
- Для конкатенации в циклах