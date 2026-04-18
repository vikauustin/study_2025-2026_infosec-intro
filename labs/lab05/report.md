---
## Front matter
title: "Лаборатораня работа №5"
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

Изучение механизмов изменения идентификаторов, применения
SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Задание

Выполнить порядок выполнения работы
1. Создание программы
2. Исследование Sticky-бита

# Выполнение лабораторной работы

Войдите в систему от имени пользователя guest, создайте программу simpleid.c, скомплилируйте программу, выполните программу simpleid, выполните системную программу id:(рис. [-@fig:001]).

![Выполняем задания](image/1.jpg){#fig:001 width=70%}

Создайте simpleid2.с, Скомпилируйте и запустите simpleid2.c, выполните проверку правильности установки новых атрибутов и смены владельца файла simpleid2, запустите simpleid2 и id:(рис. [-@fig:002]).

![Создаем файл и вставляем текст](image/2.jpg){#fig:002 width=70%}

От имени суперпользователя выполните команды:(рис. [-@fig:003]).

![Вводим следующие команды](image/3.jpg){#fig:003 width=70%}

Создайте программу readfile.c, откомпилируйте её,проверьте, может ли программа readfile прочитать файл readfile.с, Проверьте, может ли программа readfile прочитать файл /etc/shadow(рис. [-@fig:004]).

![Программа не может прочитать эти файлы](image/4.jpg){#fig:004 width=70%}

Смените владельца у файла readfile.c (или любого другого текстового файла в системе) и измените права так, чтобы только суперпользователь (root) мог прочитать его, a guest не мог(рис. [-@fig:005]).

![вводим команду](image/5.jpg){#fig:005 width=70%}

От имени пользователя guest создайте файл file01.txt в директории /tmp со словом test,просмотрите атрибуты у только что созданного файла и разрешите чтение и запись для категории пользователей «все остальные»(рис. [-@fig:006]).

![Вводим команды из туиса](image/6.jpg){#fig:006 width=70%}

От пользователя guest2 (не являющегося владельцем) попробуйте прочитать файл /tmp/file01.txt,От пользователя guest2 попробуйте дозаписать в файл /tmp/file01.txt слово test2 командой(рис. [-@fig:007]).

![Мне удалось это сделать я проверила командой cat](image/7.jpg){#fig:007 width=70%}

От пользователя guest2 попробуйте удалить файл /tmp/file01.txt командой,повысьте свои права до суперпользователя следующей командой(рис. [-@fig:008]).

![Не удалось удалить файл](image/8.jpg){#fig:008 width=70%}

Выполните после этого команду, снимающую атрибут t (Sticky-бит) с директории /tmp, покиньте режим суперпользователя командой(рис. [-@fig:009]).

![ВЫполянем команды из туиса](image/9.jpg){#fig:009 width=70%}

От пользователя guest2 проверьте, что атрибута t у директории /tmp нет, повторите предыдущие шаги(рис. [-@fig:010]).

![Ничего не изменилось](image/10.jpg){#fig:010 width=70%}

Повысьте свои права до суперпользователя и верните атрибут t на директорию /tmp(рис. [-@fig:011]).

![Выполняем задания](image/11.jpg){#fig:011 width=70%}

# Выводы

У нас получилось изучить механизмы изменения идентификаторов, применения SetUID- и Sticky-битов. Получить практические навыки работы в консоли с дополнительными атрибутами. Рассмотреть работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

