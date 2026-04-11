---
## Front matter
title: "Индивидуальный проект"
subtitle: "Третий этап"
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

Научиться основным способам взламывания с помощью утилиты Hydra.

# Задание

1. Hydra используется для подбора или взлома имени пользователя и пароля.
2. Поддерживает подбор для большого набора приложений.


# Выполнение лабораторной работы

Разорхивируем архив с паролями по умолчанию.(рис. [-@fig:001]).

![Вводим эту команду и в Kali Linux нам дает разорхивировать этот архив](image/1.jpg){#fig:001 width=70%}

Запрос к Hydra будет выглядеть примерно так:(рис. [-@fig:002]).

![Вводим, редактируя команду из туиса, которая позволит нам получить пароль](image/2.jpg){#fig:002 width=70%}

Получаем пароль(рис. [-@fig:003]).

![Пароль оказался: password](image/3.jpg){#fig:003 width=70%}

Вводим данные в ячейку(рис. [-@fig:004]).

![У нас получилось, мы подобрали пароль с помощью той команды ](image/4.jpg){#fig:004 width=70%}

# Выводы

Мы научились основным способам взламывания с помощью утилиты Hydra.

