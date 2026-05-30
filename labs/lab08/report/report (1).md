---
## Front matter
title: "Лабораторная работа №8"
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

Освоить на практике применение режима однократного гаммирования
на примере кодирования различных исходных текстов одним ключом

# Задание

1. Даны два открытых текста (телеграммы P_1 и P_2) и один секретный ключ K длиной 20 байт. Оба текста зашифрованы одним и тем же ключом в режиме однократного гаммирования (XOR).
2. Требуется, не зная ключа и не пытаясь его подобрать, восстановить содержание обоих текстов, используя только полученные шифротексты C_1 и C_2.
3. Уязвимость: при шифровании двух разных сообщений одинаковым ключом выполняется соотношение
    (ключ сокращается, так как K \oplus K = 0).
4. Атака основана на том, что формат первого сообщения частично известен (фиксированный шаблон «НаВашисходящийот…»). Используя это, из равенства
   восстанавливаются символы второго сообщения на позициях известного шаблона.
5. Полученный осмысленный фрагмент второго сообщения позволяет достроить его полностью, а затем восстановить и первое сообщение. Таким образом, оба текста читаются без расшифровки ключа.
6. В ходе работы разработано приложение на Python, которое:
   · шифрует оба текста заданным ключом;
   · выполняет описанную атаку без использования ключа;
   · выводит восстановленный фрагмент второго сообщения, что доказывает успешность взлома
   
## Выполнение

 Реализация атаки на языке Python
Здесь показан код, который(рис. [-@fig:001]).


![шифрует две телеграммы P_1 и P_2 одним ключом;использует известный шаблон P_1 ](image/1.jpg){#fig:001 width=70%}

Результат работы программы
В консоли видно восстановленный фрагмент второй телеграммы:«всеверныйфилиалб…»(рис. [-@fig:002]).

![Это доказывает, что, зная только шифротексты и формат первого сообщения, можно прочитать часть второго сообщения, не расшифровывая ключ](image/2.jpg){#fig:002 width=70%}

# Выводы
 У нас получилось освоить на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом



