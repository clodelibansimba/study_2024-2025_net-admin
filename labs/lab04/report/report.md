---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "Администрирование локальных сетей"
author: "Бансимба Клодели Дьегра, НПИбд-02-22"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib


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

Провести подготовительную работу по первоначальной настройке коммутаторов сети.

# Выполнение лабораторной работы

Создадим новый проект с названием lab_PT-04.pkt (рис. @fig:001).

![новый проект](image/0.jpg){#fig:001 width=70%}

В логической рабочей области Packet Tracer разместим коммутаторы и оконечные устройства согласно схеме сети L1 (схема приведена в лабораторной работе) и соединим их через соответствующие интерфейсы (рис. @fig:002).

![Размещение коммутаторов и оконченных устройств согласно схеме сети L1.](image/1.png){#fig:002 width=70%}

устройств согласно схеме сети L1.
Используя типовую конфигурацию коммутатора, настроем все коммутаторы, изменяя название устройства и его IP-адрес согласно плану IP (рис. @fig:003).

![Настройка коммутатора msk-donskaya-claudely-sw-1, используя типовую конфигурацию.](image/2.png){#fig:003 width=70%}


![Настройка коммутатора msk-donskaya-claudely-sw-2, используя типовую конфигурацию.](image/3.png){#fig:004 width=70%}


![Настройка коммутатора msk-donskaya-claudely-sw-3, используя типовую конфигурацию.](image/4.png){#fig:005 width=70%}


![Настройка коммутатора msk-donskaya-claudely-sw-4, используя типовую конфигурацию.](image/5.png){#fig:006 width=70%}


![Настройка коммутатора msk-pavlovskaya-claudely-sw-1, используя типовую конфигурацию.](image/6.png){#fig:007 width=70%}

# Выводы

В	ходе	выполнения	лабораторной	работы	мы	научились	проводить подготовительную работу по первоначальной настройке коммутаторов сети.

# Ответы на контрольные вопросы:

1. При помощи каких команд можно посмотреть конфигурацию сетевого оборудования? - show running-config
2. При помощи каких команд можно посмотреть стартовый конфигурационный файл оборудования? - show startup-config
3. При помощи каких команд можно экспортировать конфигурационный файл оборудования? - copy running-config startup-config/copy running-config flash
4. При помощи каких команд можно импортировать конфигурационный файл оборудования? - copy startup-config running-config

# Список литературы{.unnumbered}

::: {#refs}
:::
