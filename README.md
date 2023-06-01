# comporatorXLS
Node.js сервер для сравнения файлов Excle (каждый с каждым) на выявления расхождений

Для запуска данного приложения как служба используйте Менеджер процессов PM2
Приложение было разработано для поиска расхождений виноматериала в разных файлах Excel

Пример:
Есть файл А который содержит код ЕГАИС 01 и количество 10
Есть файл Б который содержит код ЕГАИС 01 и количество 11
Есть файл В который содержит код ЕГАИС 01 и количество 9 и  код ЕГАИС 01 и количество 1

Результат проверки будет:
в Файле А (10) есть расхождения с файлом Б (11)
в Файле В (10) есть расхождения с файлом Б (11)

Пояснение:
Сравниваются суммы ключей код ЕГАИС
ВНИМАНИЕ: Так как некоторые пользователи путаются я хочу пояснить что первая строка в файле для именования колонок
c - это ключ,
d - это значение,
x - это для пропуска (исключает строку из сравнения)
Так вот в первой строке файлов которые будут сравниваться необходимо ввести эти буквы в соответствующих колонках
(а некоторые пользователи думают что имя колонки должно быть d,c,x но это не верно! имя колонки может быть любым!)

1. Добавляем в файлах (которые будем сравнивать) пустую первую строку
2. Задаем в добавленной первой пустой строке значение в колонках которые отвечают за ключ (c), количество (d)
3. Нажимаем "Выбрать файлы" (это множественный выбор) необходимо выбрать сразу все файлы который надо сравнить и нажать "Открыть"
4. Нажимаем "Выполнить"
