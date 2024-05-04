##  Drivers_Synology_DSM_7
# Драйверы для ключей Wi-Fi, USB-ключей цифровых телевизоров и т. д. Для Synology DSM 7

Эти файлы позволяют использовать USB-ключи, такие как Wi-Fi, DTV и т. д., для Synology DSM 7.

Выберите свою архитектуру и поместите ее в /lib/modules вашего NAS. 

Смотрите на офф сайте вашу архитектуру

Затем вам необходимо запустить через SSH следующие команды:

`sudo -i`

`/sbin/modprobe usbserial`

`/sbin/modprobe ftdi_sio`

`/sbin/modprobe cdc-acm`

`chmod 777 /dev/ttyUSB0`

`chmod 777 /dev/ttyACM0`

`sudo ./lib/modules/start-usb-drivers.sh`



