# Настройка Betaflight

Подключиться к полётному контроллеру посредством Betaflight configurator.&#x20;

Перейти во вкладку консоли и последовательно ввести следующие команды:&#x20;

```
set osd_displayport_device = MSP
```

```
set displayport_msp_serial = <ConfiguratorUART - 1>
```

{% hint style="info" %}
где \<ConfiguratorUART - 1> = номер порта в конфигураторе, куда подключены AirUnit/CaddxVista уменьшенный на 1 (если UART1 то set displayport\_msp\_serial = 0, если UART2, то set displayport\_msp\_serial = 1 и т.д.)
{% endhint %}

```
set vcd_video_system = PAL
```

```
save
```

&#x20;Проверить, после настройки, можно командой&#x20;

```
get displayport_msp_serial
```

{% hint style="warning" %}
&#x20;Крайне не рекомендуется использовать softserial
{% endhint %}

После успешной установки, после загрузки очков в левом нижнем углу появится сообщение «OSD waiting…»

