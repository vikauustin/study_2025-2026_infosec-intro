---
## Front matter
title: "Индивидуальный проект"
subtitle: "Первый этап"
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

Научиться основным способам тестирования веб приложений.

# Задание

Установить необходимое программное обеспечение.Настроить и войти в систему 

# Выполнение лабораторной работы

Установите дистрибутив Kali Linux в виртуальную машину.(рис. [-@fig:001]).

![Задаем настройки для kaliи запускаем первый раз машину](image/1.jpg){#fig:001 width=70%}

Открывается первоначальное окно(рис. [-@fig:002]).

![Выбираем: graphical incstall и ждем пока загрузится](image/2.jpg){#fig:002 width=70%}

Настройка учетный записей пользователя(рис. [-@fig:003]).

![Выбираем пароль для пользователя(нас)](image/3.jpg){#fig:003 width=70%}

Настройка времени(рис. [-@fig:004]).

![Выбираем московское время](image/4.jpg){#fig:004 width=70%}

Разметка дисков(рис. [-@fig:005]).

![Выбираем: закончить попытку и записать изменения на диск](image/5.jpg){#fig:005 width=70%}

Выбор программного опеспечения (рис. [-@fig:006]).

![Выбираем все кроме: GNOME, KDE Plasma и ждем когда система завершит загрузку](image/6.jpg){#fig:006 width=70%}

После всех остальныех настроек и загрузки:(рис. [-@fig:007]).

![Kali открылся, значит у нас получилось все установить и скачать](image/7.jpg){#fig:007 width=70%}

# Выводы

Выполнение первого этапа индивидуального проекта прошло успешно, а также получилось войти в новую систему Kali Linux


