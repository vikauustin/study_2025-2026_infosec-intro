---
## Front matter
title: "Использование nikto"
subtitle: "Report"
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

Научиться основным способам использования nikto

# Задание

1. nikto — базовый сканер безопасности веб-сервера. Он сканирует и обнаруживает уязвимости в веб-приложениях, обычно вызванные неправильной конфигурацией на самом сервере, файлами, установленными по умолчанию, и небезопасными файлами, а также устаревшими серверными приложениями.

# Выполнение лабораторной работы

Проверяем скачан ли nikto (рис. [-@fig:001]).

![Так как мы видим его версию, соответсвенно он скачан](image/1.jpg){#fig:001 width=70%}

Проверяем какие утилиты у него есть (рис. [-@fig:002]).

![Смотрим основные команды снизу](image/2.jpg){#fig:002 width=70%}

Вводим основную команду и смотрим вывод(рис. [-@fig:003]).

![Следующий слайд](image/3.jpg){#fig:003 width=70%}

1. The anti-clickjacking X-Frame-Options header is not present.
 сайт не запрещает другим сайтам вставлять себя во фрейм. Этим могут воспользоваться злоумышленники: они поместят ваш сайт внутрь своего сайта, а поверх наложат невидимые кнопки. Когда вы будете кликать по картинкам, на самом деле будете нажимать на скрытую кнопку «Перевести деньги». Это называется clickjacking.
2. The X-Content-Type-Options header is not set.
Браузер иногда сам угадывает тип файла (например, файл .txt пытается выполнить как JavaScript). Хакеры могут этим воспользоваться, загрузив на сайт картинку, внутри которой написан вредоносный скрипт. Браузер может по ошибке выполнить его.
3. Root page /DVWA redirects to: login.php
Это не уязвимость, а особенность. Просто при переходе на http://localhost/DVWA сервер отправляет вас на страницу входа login.php. Это нормально для приложений с авторизацией.
4. /DVWA/config/: Directory indexing found.
Если вы откроете в браузере http://localhost/DVWA/config/, вы увидите список всех файлов в этой папке. Поскольку в /config/ обычно лежат важные настройки (файлы с паролями к базе данных, ключи шифрования), любой, кто знает путь, сможет их скачать.(рис. [-@fig:004]).

# Выводы

Мы научились основным способам использования nikto

