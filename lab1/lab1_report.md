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
Целью данной работы является развертывание виртуальной машины на базе платформы Yandex compute cloud с установленной системой контроля конфигураций Ansible и установка CHR в VirtualBox

Ход работы:
    1) Была создана виртуальная машина на платформе Yandex compute cloud с необходимыми характеристиками.  
    ![Image text](screens/1.PNG)  
    2) Было произведено подключени по SSH к виртуальной машине при помощи пары заранее сгенерированных ключей, публичный ключ был занесен на платформу Yandex compute cloud.  
    ![Image text](screens/2.PNG)  
    ![Image text](screens/3.PNG)  
    3) На виртуальную машину был установлен Ansible и python3.8  
    ![Image text](screens/4.PNG)  
    4) В VirtualBox была создана виртуальная машина RouterOS на основе образа, представленного на оффициальном сайте. Для корректной работы виртуальной машины тип подключения в настройках была обозначен как "Сетевой мост". В дальнейшем подключение будет производится по MAC-адресу.  
    ![Image text](screens/5.PNG)  
    5) Для организации VPN туннеля было выбрано решение Wireguard. На удаленном сервере была сгенерирована и сохранена пара ключей при помощи утилит, предоставляемых Wireguard-ом.  
    ![Image text](screens/6.PNG)  
    6) Была выполнена конфигурация Wireguard-сервера на удаленной машине, обозначен используемый порт, разрешенный адрес пира (RouterOS), значение ключей.  
    ![Image text](screens/20.PNG)  
    7) Для конфигурации клиента на RouterOS был использован Winbox. Был сконфигурирован интерфейс wireguard1.  
    ![Image text](screens/7.PNG)  
    8) В список пиров для Wireguard был добавлен Wireguard-сервер, заполнено значение порта, IP-адрес, публичный ключ сервера.  
    ![Image text](screens/8.PNG)  
    9) Были сохранены ip-адреса интерфейсов. На интерфейс wireguard1 был сохранен адрес, ранее записанный для пира на сервере.  
    ![Image text](screens/9.PNG)  
    10) Был настроен DHCP-клиент. Это не обязательная настройка для поднятия Wireguard туннеля, но моя локальная сеть использует DHCP-сервер.  
    ![Image text](screens/10.PNG)  
    ![Image text](screens/11.PNG)  
    После этого Wireguard-сервер начинает видеть подключенный пир, машины пингуются друг другом.  
    ![Image text](screens/12.PNG)  
    ![Image text](screens/13.PNG)  
Вывод:
    Были созданы виртуальные машины: на облачной платформе и локально. Был создан сервер автоматизации на платформе Yandex compute cloud, настроен VPN-туннель при помощи решения Wireguard, проверена корректная работа элементов. 