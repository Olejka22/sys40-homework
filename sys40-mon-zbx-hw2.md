# Домашнее задание к занятию 
# "`Система мониторинга Zabbix. Часть 2`" - `Ольга Антоненко`

### Задание 1

`Создайте свой шаблон, в котором будут элементы данных, мониторящие загрузку CPU и RAM хоста.`

   1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
   2. В веб-интерфейсе Zabbix Servera в разделе Templates создайте новый шаблон
   3. Создайте Item который будет собирать информацию об загрузке CPU в процентах
   4. Создайте Item который будет собирать информацию об загрузке RAM в процентах

#### Cкриншоты:
##### Шаблон:
![Скриншот-1](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx21-1.png)
##### Items:
![Скриншот-2](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx21-2.png)
##### Latest data:
![Скриншот-3](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx21-3.png)

---

### Задание 2

`Установите Zabbix Agent на два хоста.`

   1. Выполняя ДЗ, сверяйтесь с процессом отражённым в записи лекции.
   2. Установите Zabbix Agent на 2 вирт.машины, одной из них может быть ваш Zabbix Server.
   3. Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов.
   4. Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera.
   5. Проверьте, что в разделе Latest Data начали появляться данные с добавленных агентов.

#### Cкриншоты:
##### Хосты
![Скриншот-1](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx12-1.png)
##### Лог запуска агента
![Скриншот-2](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx12-2.png)
##### Данные с агента
![Скриншот-3](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx12-3.png)
##### Данные с сервера
![Скриншот-4](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx12-4.png)

#### Команды
```
sudo -s

apt install zabbix-agent
sed -i 's/Server=127.0.0.1/Server=192.168.1.10/g' /etc/zabbix/zabbix_agentd.conf
sed -i 's/ServerActive=127.0.0.1/ServerActive=192.168.1.10/g' /etc/zabbix/zabbix_agentd.conf

systemctl restart zabbix-agent
systemctl enable zabbix-agent
```
---

### Задание 3

`Установите Zabbix Agent на Windows (компьютер) и подключите его к серверу Zabbix.`

   1. Приложите в файл README.md скриншот раздела Latest Data, где видно свободное место на диске C:

#### Cкриншоты:
![Скриншот-1](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx13-1.png)<br>
![Скриншот-2](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx13-2.png)<br>
![Скриншот-3](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx13-3.png)<br>
![Скриншот-4](https://github.com/Olejka22/sys40-homework/blob/main/img/zbx13-4.png)
