---
## Front matter
title: "Лаборатораня работа №3"
subtitle: "Отчет"
author: "Устинова Виктория Вадимовна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей

# Задание

Дискреционное разграничение прав в Linux. Два пользовател


# Выполнение лабораторной работы

В установленной операционной системе создайте учётную запись пользователя guest2, задайте пароль для пользователя guest2(рис. [-@fig:001]).

![создаем нового пользователя и задаем ему пароль](image/1.jpg){#fig:001 width=70%}

Добавьте пользователя guest2 в группу guest:(рис. [-@fig:002]).

![вводим новую команду](image/2.jpg){#fig:002 width=70%}

Осуществите вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли(рис. [-@fig:003]).

![Входим в пользователей](image/3.jpg){#fig:003 width=70%}

Осуществите вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли(рис. [-@fig:004]).

![Входим в пользователей и смотрим директорию](image/4.jpg){#fig:004 width=70%}

Определите командами groups guest и groups guest2, в какие группы входят пользователи guest и guest2. Сравните вывод команды groups с выводом команд id -Gn и id -G.(рис. [-@fig:005]).

![Группа guest](image/5.jpg){#fig:005 width=70%}

Определите командами groups guest и groups guest2, в какие группы входят пользователи guest и guest2. Сравните вывод команды groups с выводом команд id -Gn и id -G.(рис. [-@fig:006]).

![Группы guest and guesr2](image/6.jpg){#fig:006 width=70%}

Сравните полученную информацию с содержимым файла /etc/group, от имени пользователя guest измените права директории /home/guest, разрешив все действия для пользователей группы:(рис. [-@fig:007]).

![Одинаковый вывод](image/7.jpg){#fig:007 width=70%}

От имени пользователя guest снимите с директории /home/guest/dir1, и проверьте правильность снятия атрибутов(рис. [-@fig:008]).

![Сняты верно](image/8.jpg){#fig:008 width=70%}

# Выводы

Мы успешно получили практические навыки работы в консоли с атрибутами файлов для групп пользователей


