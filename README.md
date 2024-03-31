# RK-1
# Выполнила Федотова Екатерина ИУ8-23
# cpp-cheat-sheet
Шпаргалка по базовым структурам данныхх и алгоритмам С++.
Ссылка на репозиторий: https://github.com/gibsjose/cpp-cheat-sheet


3. Количество файлов
```bash
$ git ls-files | wc -l
```
```
39
```
4. Объем всех файлов
```bash
$ git ls-files | xargs wc -c | awk '{total += $1} END {print total}'
```
```
6348870
```
5. Объем исходного кода: cpp, c, h, hpp, cxx, py, pl, php, java, cs, rb, rs, hs
```bash
$ git ls-files | grep -E ".(cpp|c|h|hpp|cxx|py|pl|php|java|cs|rb|rs|hs)$" | xargs wc -c | awk '{total += $1} END {print total}'
```
```
10456
```
6. Найти, если есть файл .clang-format
```bash
$ find . -type f -name ".clang-format"
```
```
Пустой вывод - нет .clang-format
```

7. Если есть каталог src, то общее количество файлов в каталоге src
```bash
$ find src -type f | wc -l
```
```
find: ‘src’: Нет такого файла или каталога
```
8. Выписать количество файлов, содержащих слово socket независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -l -i "socket" | wc -l
```
```
0
```
9. Выписать количество файлов, содержащих слово select независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -l -i "select" | wc -l
```
```
2
```
10. Выписать количество раз, сколько, содержится слово Microsoft, Google или Intel независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -i -e "Microsoft" -e "Google" -e "Intel" | wc -l
```
```
3
```
11. Найти расположение файла LICENSE относительно начала репозитория.
```bash
$ find . -name LICENSE*
```
```
Пустой вывод - нет файла LICENSE
```
12. Вывести строку для файла LICENSE (если он есть), содержащую следующие подпоследовательности символов: BSD, GNU, MIT, APSL, Apache, GPL, AGPL, LGPL
```bash
$ grep -e "BSD" -e "GNU" -e "MIT" -e "APSL" -e "Apache" -e "GPL" -e "AGPL" -e "LGPL" LICENSE.txt
```
```
Нет такого файла 
```
