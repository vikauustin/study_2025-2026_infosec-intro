---
## Front matter
title: "Лаборатораня работа №2"
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

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux1.

# Задание

Выполнить: последовательность выполнения работы.
написать отчет.

# Выполнение лабораторной работы

В установленной при выполнении предыдущей лабораторной работы операционной системе создайте учётную запись пользователя guest(рис. [-@fig:001]).

![Дополнительно задаем пароль для пользователя, и входим в систему от нового п.](image/1.jpg){#fig:001 width=70%}

Определите директорию, в которой вы находитесь, командой pwd, уточните имя вашего пользователя командой, Сравните вывод id с выводом команды groups(рис. [-@fig:002]).

![Мы по именем guest, находимся в домашней директории](image/2.jpg){#fig:002 width=70%}

Просмотрите файл /etc/passwd командой(рис. [-@fig:003]).

![смотрим файл](image/3.jpg){#fig:003 width=70%}

Найдите в нём свою учётную запись.(рис. [-@fig:004]).

![Находим с помощью команды](image/4.jpg){#fig:004 width=70%}

Определите существующие в системе директории командой, Проверьте, какие расширенные атрибуты установлены на поддиректориях, находящихся в директории /home, командой:(рис. [-@fig:005]).

![вводим команды](image/5.jpg){#fig:005 width=70%}

Создайте в домашней директории поддиректорию dir1 командой, определите командами ls -l и lsattr, какие права доступа и расширенные атрибуты были выставлены на директорию dir1.(рис. [-@fig:006]).

![drwxr-xr-x](image/6.jpg){#fig:006 width=70%}

Определите командами ls -l и lsattr, какие права доступа и расширенные атрибуты были выставлены на директорию dir1.(рис. [-@fig:007]).

![Выполняем команду lsattr](image/7.jpg){#fig:007 width=70%}

Снимите с директории dir1 все атрибуты командой, и проверьте с её помощью правильность выполнения команды, попытайтесь создать в директории dir1 файл file1 командой(рис. [-@fig:008]).

![Нам нельзя создать файл после снятия прав](image/8.jpg){#fig:008 width=70%}


# Выводы

У нас получилось получить практические навыки работы в консоли с атрибутами файлов, закрепить теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux1.


