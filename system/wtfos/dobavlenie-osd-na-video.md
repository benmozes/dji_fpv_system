# Добавление OSD на видео

На ресурсе developer-сборки (пререлизный ресурс проекта WFTOS) есть возможность наложить записанные данные на файл DVR полета.&#x20;

Для записи данных ОСД в файл нужно подключить очки с Root-доступом к компьютеру и в консоли конфигуратора WTFOS CLI ввести следующие команды:&#x20;

{% code lineNumbers="true" %}
```
package-config set msp-osd rec_enabled true
package-config apply msp-osd
```
{% endcode %}

Рендерер доступен по [ссылке](https://knifa-develop.fpv.wtf/osd-overlay).

{% hint style="warning" %}
Можно использовать только видео DVR очков, другие видеофайлы нормально не рендерятся и вызывают проблемы в работе рендерера
{% endhint %}
