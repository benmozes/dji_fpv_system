---
description: часто задаваемые вопросы
---

# F.A.Q.

### Можно ли использовать очки из DJI FPV Drone kit совместно с Air Unit/Caddx Vista?

да, можно

### **Как далеко можно улететь?**

лимит около 13.3-13.4 км

### **Как включить режим 50Мбит?**

1. прошить очки и передатчик на прошивку выше v01.00.06.00
2. обязательно переключить канал на какой-то из 1-3 (на CH8 public 50Мбит не работает)

![](https://djifpv.ru/FAQ/pics/50mbps.jpg?raw=true)

![](https://djifpv.ru/FAQ/pics/50mbps.png?raw=true)

### **Есть засветы по углам на стоковой маске, как быть?**

Купить [новую](../system/aksessuary/maski.md) или напечатать [проставки](https://www.thingiverse.com/thing:3840374)

### **Как увеличить мощность выше 25мВт**&#x20;

Сделать [FCC Hack](../system/fcc-hack.md)

### **Как включить кастом OSD?**

#### Betaflight

* Активировать порт на который припаяли RX и TX;

![](https://djifpv.ru/FAQ/pics/betaports.jpg?raw=true)

* Включить OSD

![](https://djifpv.ru/FAQ/pics/betaOSD.jpg?raw=true)

#### KiSS:

*   Выбрать в [Serial configuration](https://raw.githubusercontent.com/benmozes/djifpvrus/master/FAQ/pics/kiss.png) DJI-MSP на нужном порту.



![](https://djifpv.ru/FAQ/pics/kiss.png?raw=true)

* Не забудьте включить в настройках **очков** custom OSD:
  * settings
  * display
  * custom OSD - on

### **Что есть в Betaflight OSD до патчей?**

|                              | по состоянию на август 2020        |
| ---------------------------- | ---------------------------------- |
| ~~Adjustment range~~         | GPS stats                          |
| Altitude                     | GPS speed                          |
| Angle: pitch                 | Home direction                     |
| Angle: roll                  | Home distance                      |
| ~~Anti gravity~~             | ~~Link quality~~                   |
| ~~Artifical horizon~~        | ~~Motor diagnostics~~              |
| Artifical horizon sidebars   | ~~Numerical heading~~              |
| Battery average cell voltage | Numercial vario                    |
| Battery current draw         | PID pitch                          |
| Battery current mAh drawn    | PID roll                           |
| ~~Battery efficiency~~       | PID yaw                            |
| Battery usage                | Power                              |
| Battery voltage              | ~~Profile: OSD profile name~~      |
| ~~Blackbox log status~~      | Profile: PID and rate              |
| ~~Camera frame~~             | ~~Profile: PID profile name~~      |
| ~~Compass bar~~              | ~~Profile: PID rate profile name~~ |
| ~~Core temperature~~         | ~~RC Channels~~                    |
| Craft name                   | ~~RSSI dBm value~~                 |
| Crosshairs                   | RSSI value                         |
| ~~Debug~~                    | RTC date and time                  |
| Disarmed                     | ~~Stick overlay left~~             |
| ~~ESC RPM~~                  | ~~Stick overlay right~~            |
| ~~ESC RPM frequency~~        | ~~Throttle position~~              |
| ESC Temperature              | ~~Timer 1~~                        |
| ~~Flight distance~~          | ~~Timer 2~~                        |
| ~~Flip after crash arrow~~   | ~~Timer: remaining time estimate~~ |
| Fly mode                     | ~~VTX channel~~                    |
| ~~G force~~                  | ~~Warning~~                        |
| GPS latitude                 | ~~Display name~~                   |
| GPS longtitude               |                                    |

### **Непонятные координаты в OSD, как починить?**

Если на OSD вот такие координаты, что не хватает последней цифры (должно быть 7 знаков после точки), то в этой координате надо после точки добавить ноль, и после этого вбивать в гугл. Иначе может показать в стороне на десятки километров.

![](https://djifpv.ru/FAQ/pics/badOSD.png?raw=true)

### **Не работает кастом OSD**

> RX\&TX на нужном месте, в настройках всё выставлено правильно, всё перепроверил **(3 раза, крайне внимательно)**
>
> Баг точно встречался на Vista, когда прошивали модуль с включёнными очками. Возможно, работает и для Air Unit.
>
> **На некоторых полётниках (mamba f722 mini, например) передатчик некорректно работает на конкретных UART, попробуйте подключить к другому.**
>
> _если вы столкнулись с такой проблемой, напишите пожалуйста в чате название полётника, UART на котором передатчик работал/работает некорректно, составим список и внесём сюда._
>
> Если вы провели downgrade\&upgrade прошивки с выключенными очками, проверили все UART, а custom OSD по-прежнему не работает - может помочь редкий кейс  Все приведённые выше манипуляции вы проводите на свой страх и риск!

### **Выпадает кабель питания из очков, что делать**

> Рандомный случай, у кого-то держится отлично, у кого-то вываливается, вариантов пофиксить несколько:
>
> * Закрепить кабель на [стяжку](https://t.me/djifpvrus/11332);
> * Напечатать:
>   * с держалкой;
>   * Или [держалку](https://www.thingiverse.com/thing:4170116);

### **Надо ли менять стоковые антенны?**

> Не обязательно, **вообще не обязательно -** [13](https://t.me/djifpvrus/19040) - [14](https://t.me/djifpvrus/19054) км пруфы, менять стоит только в погоне за long range или компактностью (ну или просто “потому что могу”).

### **Какой разъём должен быть у антенн для очков?**

> RP-SMA.

### **Можно ли летать на аналоге?**

> С помощью модификации - да.

### **Какой аналог мод выбрать**

> * .

### **Можно ли передавать видео из очков?**

> * с нюансами (не пишется DVR на очки и нет клиентов для iOS девайсов) - **да**, инструкция на отдельной [странице](https://djifpv.ru/video\_out/);
> * полноценно для V1 пока только с помощью [аксессуара](https://www.dji.com/ru/smart-controller);
> * полноценно для V2 с помощью [аксессуара](https://www.dji.com/ru/smart-controller) или **только видео с DJI drone** на телефон;

### **Как передать видео на вторые очки?**

> С помощью [audience mode](https://youtu.be/RZdYvuttQuA) (работает только в режиме 25 Мбит)

### **В очках есть jack 3.5, можно ли подключить наушники и слушать live audio во время полёта?**

> Live audio передаётся с DJI drone на v2 очки. DVR так же пишется со звуком. Звук передается в случае включения опции Audio Recording в меню очков.
>
> <img src="https://djifpv.ru/FAQ/pics/sound.jpg?raw=true" alt="sound" data-size="original">
>
> ***
>
> Для v1 очков и v2 + dji air unit/caddx vista - по-прежнему недоступно.

### **Где купить мягкую сумку для очков?**

> Стоковой сумки нет в продаже, максимально похожий вариант: [Ethix goggles pouch](https://www.team-blacksheep.com/products/prod:ethix\_goggle\_pouch)

### **Можно ли сделать угол обзора шире?**

> Можно поменять линзу, точно работает для [стандартной камеры](https://t.me/djifpvrus/98861), вероятно, работает для Caddx Nebula Pro, т.к. [одинаковые линзы](https://djifpv.ru/unit-vs-vista/) с DJI Camera: [RunCam RC18G](https://aliexpress.ru/item/4000007230138.html).
>
> * [видеоинструкция](https://youtu.be/GS9uhdzoNmA)
> * [обзор](https://youtu.be/xbOct8rGkyc) от Oleg Stelmakh

### **Как наложить на OSD телеметрию на видео?**

> 1. Записать лог телеметрии в пульте - [как настроить запись по арму](https://oscarliang.com/log-gps-coordinates-taranis/)
> 2. Полученный лог закинуть в [конвертор](https://maxbl4.github.io/otx/index.html)
>    1. OpenTx записывает все полёты за день в один файл, после парсинга выбрать нужный полёт
>    2. Перейти на вкладку Export SRT, убрать галочки с лишних пунктов (например не стоит всем показывать координаты вашего дома) и нажать Export. Вы получите SRT файл, который можно назвать также как ваше видео и он автоматом откроется в плеере. При желании можно вшить субтитры в видео с помощью FFMPEG
> 3. Если хотите красивое OSD, можно лог загруженный в пункте 2.1 экспортировать в CSV и этот файл передать в [DashWare](http://www.dashware.net/), но там требуется довольно нудная настройка

### **Как исправить вылет на заставку DJI при слабом сигнале аналог мода?**

Необходимо переключить из PAL в NTSC

{% embed url="https://t.me/djifpvrus/199861" %}
PAL
{% endembed %}

{% embed url="https://t.me/djifpvrus/199864" %}
NTSC
{% endembed %}

