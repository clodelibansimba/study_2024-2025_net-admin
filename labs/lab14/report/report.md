---
## Front matter
title: "Отчёт по лабораторной работе №14"
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

Настроить взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.

# Выполнение лабораторной работы

Теперь откроем проект с названием lab_PT-13.pkt и сохраним под названием lab_PT-14.pkt. После чего откроем его для дальнейшего редактирования (рис. @fig:001).

![нОткрытие проекта lab_PT-14.pkt.](image/1.png){#fig:001 width=70%}

Первым делом нам нужно настроить линку между площадками. Для этого настроим интерфейсы у коммутатора provider-claudely-sw-1, маршрутизатора msk-donskaya-claudely-gw-1, маршрутизатора msk-q42-claude-gw-1, коммутатора sch-sochi-claude-sw-1 и маршрутизатора sch-sochi-claude-gw-1

![Настройка интерфейсов коммутатора provider-claudely-sw-1](image/2.png){#fig:002 width=70%}


![Настройка интерфейсов маршрутизатора msk-donskaya-claudely-gw-1.](image/1.png){#fig:003 width=70%}

![несение изменений в схему L1 сети (добавление информации о сети основной территории (42-й квартал в Москве) и сети филиала в г. Сочи).](image/3.png){#fig:004 width=70%}

![Настройка интерфейсов маршрутизатора msk-q42-claude-gw-1.](image/4.png){#fig:005 width=70%}

![Настройка интерфейсов коммутатора sch-sochi-claude-sw-1.](image/6.png){#fig:006 width=70%}

![Настройка интерфейсов маршрутизатора sch-sochi-claude-gw-1.](image/7.png){#fig:007 width=70%}

Следующим шагом настроим площадку 42-го квартала. Для этого настроим интерфейсы у маршрутизатора msk-q42-claude-gw-1, коммутатора msk-q42-claude-sw-1, маршрутизирующего коммутатора msk-hostel-claude-gw-1 и коммутатора msk-hostel-sw-1

![Настройка интерфейсов маршрутизатора msk-q42-claude-gw-1.](image/9.png){#fig:008 width=70%}

![Настройка интерфейсов коммутатора msk-q42-claude-sw-1.](image/10.png){#fig:009 width=70%}

![Присвоение адресов оконечному устройству pc-q42-1.](image/11.png){#fig:010 width=70%}

![Выполнение проверки.](image/12.png){#fig:011 width=70%}

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-claude-gw-1](image/13.png){#fig:012 width=70%}


Далее настроим площадку в Сочи. Настроим интерфейсы у маршрутизатора sch-sochi-claude-gw-1 и у коммутатора sch-sochi-claude-sw-1

![Первоначальная настройка маршрутизатора sch-sochi-claude-gw-1.](image/18.png){#fig:013 width=70%}

![Первоначальная настройка коммутатора sch-sochi-claude-sw-1.](image/19.png){#fig:014 width=70%}

атем настроим маршрутизацию между площадками. Настроим маршрутизатор msk-donskaya-claudely-gw-1, маршрутизатор msk-q42-claude-gw-1 и маршрутизатор sch-sochi-claude-gw-1

![Настройка маршрутизатора msk-donskaya-claudely-gw-1.](image/21.png){#fig:015 width=70%}

![Настройка маршрутизатора msk-q42-claude-gw-1.](image/23.png){#fig:016 width=70%}

![Настройка маршрутизатора sch-sochi-claude-gw-1.](image/25.png){#fig:017 width=70%}


Предпоследним шагом настроим маршрутизацию на 42 квартале. Для этого настроим маршрутизатор msk-q42-claude-gw-1 (Рис. 1.26) и маршрутизирующий коммутатор msk-hostel-claude-gw-1

![Настройка маршрутизатора msk-q42-claude-gw-1.](image/26.png){#fig:018 width=70%}

![ННастройка интерфейсов маршрутизирующего коммутатора msk-hostel-claude-gw-1.](image/27.png){#fig:019 width=70%}

И наконец последним шагом настроим NAT на маршрутизаторе msk-donskaya-claudely-gw-1 (Рис. 1.28) и выполним контрольную проверку

![Настройка NAT на маршрутизаторе msk-donskaya-claudely-gw-1.](image/28.png){#fig:020 width=70%}

# Выводы
В ходе выполнения лабораторной работы мы настроили взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.



# Ответы на контрольные вопросы:

1.  Приведите пример настройки статической маршрутизации между двумя подсетями организации. - Необходимо задать IP шлюзов на интерфейсах, настроить sub-интерфейсы с тегированием кадром VLAN'ами и своими IP, затем настроить статические маршруты между сетями.
2.  Опишите процесс обращения устройства из одного VLAN к устройству из другого VLAN. - 1 устройство посылает фрейм на маршрутизатор, тот меняет MAC исходника на свой и перенаправляет фрейм 2 устройству.
3.  Как проверить работоспособность маршрута? - ping на диаметрально противоположных устройствах друг к другу.
4.  Как посмотреть таблицу маршрутизации? - show ip route
