
##RK 1


_____
Current task: 1

1. Название проекта:

RTTR

____
Current task: 2

2. описание проекта:
RTTR означает «Отражение типа времени выполнения». Он описывает способность компьютерной программы анализировать и изменять объект во время выполнения.


_____
Current task: 3

3. Количество файлов

script:
```bash
$ find -type f | wc -l
```

result:
`555`


_____
Current task: 4

4. Объем всех файлов

script:
```shell
$ du -csh
```

result:
```
16M	.
16M	total
```

_____
Current task: 5

5. Объем исходного кода: cpp, c, h, hpp, cxx, py, pl, php, java, cs, rb, rs, hs

script:
```shell
$ cloc ~/RK1/rttr
```

result:
```shell
     521 text files.
     468 unique files.                                          
      65 files ignored.

github.com/AlDanial/cloc v 1.90  T=0.40 s (1139.7 files/s, 348757.5 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C/C++ Header                   254          14253          22409          55033
C++                            120           6817           5518          25021
Markdown                        26            510              0           2016
CSS                              9            369             88           1788
CMake                           31            384            993           1717
SVG                              2              0              0            839
Smarty                           1             29              4            706
HTML                             6            146             20            331
YAML                             3             47            107            327
JavaScript                       5             59             65            255
-------------------------------------------------------------------------------
SUM:                           457          22614          29204          88033
-------------------------------------------------------------------------------
```

_____
Current task: 6

6. Найти, если есть файл .clang-format

script:
```shell
$ find . -type f -name "*.clang-format" | wc -l
```

result:
`0`

______
Current task: 7

7. Если есть каталог src, то общее количество файлов в каталоге src

script:
```shell
$ find ./src -type f | wc -l
```

result:
`328`


_____
Current task: 8

8. Выписать количество файлов, содержащих слово socket независимо от написания строчными или прописными буквами во всех файлах репозитория.

script:
```shell
$ find . -type f -iname "*socket" | wc -l
```

result:
`0`


______
Current task: 9

9. Выписать количество файлов, содержащих слово select независимо от написания строчными или прописными буквами во всех файлах репозитория.

script:
```shel
$ find . -type f -iname "*select" | wc -l
```

result:
`0`

_____
Current task: 10

10. Выписать количество раз, сколько, содержится слово Microsoft, Google или Intel независимо от написания строчными или прописными буквами во всех файлах репозитория.

script:
```shell
$ find . -type f -exec grep -iEo "microsoft|google|intel" {} + | wc -l
```

result:
`38`

______
Current task: 11

11. Найти расположение файла LICENSE относительно начала репозитория.

script:
```shell
$ find $(pwd) -name "LICENSE*"
```

result:
`/home/jamalay/RK1/rttr/LICENSE.txt`

____
Current task: 12

12. Вывести строку для файла LICENSE (если он есть), содержащую следующие подпоследовательности символов: BSD, GNU, MIT, APSL, Apache, GPL, AGPL, LGPL

script:
```shell
$ grep -iE "BSD|GNU|MIT|APSL|Apache|GPL|AGPL|LGPL" /home/jamalay/RK1/rttr/LICENSE.txt
```

result:
```shel
MIT License
in the Software without restriction, including without limitation the rights
copies of the Software, and to permit persons to whom the Software is
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
```



