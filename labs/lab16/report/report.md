---
## Front matter
title: "Отчёт по лабораторной работе №16"
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

Получить навыки настройки VPN-туннеля через незащищённое Интернет-соединение.

# Выполнение лабораторной работы

Откроем проект с названием lab_PT-15.pkt и сохраним под названием lab_PT-16.pkt. После чего откроем его для дальнейшего редактирования (рис. @fig:001).

![Открытие проекта lab_PT-16.pkt.](image/1.png){#fig:001 width=70%}

Разместим в рабочей области проекта в соответствии с модельными предположениями оборудование для сети Университета г. Пиза

![Замена модулей на Repeater-PT.](image/3.png){#fig:002 width=70%}

![Подключение оборудования.В физической рабочей области проекта создадим город Пиза, здание Университета г. Пиза. Переместим туда соответствующее оборудование  ](image/4.png){#fig:003 width=70%}

![Создание города Пиза в физической рабочей области.](image/5.png){#fig:004 width=70%}

![Перемещение оборудования.Теперь сделаем первоначальную настройку и настройку интерфейсов оборудования сети Университета г. Пиза ](image/6.png){#fig:005 width=70%}



![Первоначальная настройка маршрутизатора pisa-unipi-claude-gw-1.](image/7.png){#fig:006 width=70%}

![Первоначальная настройка коммутатора pisa-unipi-claude-sw-1.](image/8.png){#fig:007 width=70%}

![Настройка интерфейсов маршрутизатора pisa-unipi-claude-gw-1.](image/9.png){#fig:008 width=70%}

![Настройка интерфейсов маршрутизатора pisa-unipi-claude-gw-1.](image/10.png){#fig:009 width=70%}

![Присвоение адресов оконечному устройству.](image/11.png){#fig:010 width=70%}

![Пинг адреса 10.131.0.1.](image/12.png){#fig:011 width=70%}


Далее настроим VPN на основе протокола GRE [25] 

![Настройка маршрутизатора msk-donskaya-claudehorin-gw-1.](image/13.png){#fig:012 width=70%}

![Настройка маршрутизатора pisa-unipi-claude-gw-1.] (image/1.png){#fig:001 width=70%}%}

# Выводы

В ходе выполнения лабораторной работы мы получили навыки настройки VPN-туннеля через незащищённое Интернет-соединение.


# Ответы на контрольные вопросы:

1.  Что такое VPN? - Зашифрованное соединение, устанавливаемое через Интернет между устройством и сетью.
2.  В каких случаях следует использовать VPN? - Для дополнительного шифрования в сетях, безопасному подключению к локальным сетям извне.
3.  Как с помощью VPN обойти NAT? - Поднять VPN-туннель/подключить OpenVPN.
