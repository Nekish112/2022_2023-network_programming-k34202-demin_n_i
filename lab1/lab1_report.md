University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)
Year: 2022/2023
Group: K34202
Author: Demin Nikita Igorevich
Lab: Lab1
Date of create: 06.03.2023
Date of finished: 

Цель работы
Целью данной работы является развертывание виртуальной машины на базе платформы Microsoft Azure с установленной системой контроля конфигураций Ansible и установка CHR в VirtualBox

Ход работы:
    1) Была создана виртуальная машина на платформе Yandex compute cloud
    [alt text](screens/1.PNG?raw=true "1")
    2) Было произведено подключени по SSH к виртуальной машине
    [alt text](screens/2.PNG?raw=true "2")
    [alt text](screens/3.PNG?raw=true "3")
    3) На виртуальную машину был установлен Ansible и python3.8
    [alt text](screens/4.PNG?raw=true "4")
    4) В VirtualBox была создана виртуальная машина на CHR
    [alt text](screens/5.PNG?raw=true "5")
    5) Для организации VPN туннеля было выбрано решение Wireguard. На удаленном сервере была сгенерирована и сохранена пара ключей
    [alt text](screens/6.PNG?raw=true "6")
    6)