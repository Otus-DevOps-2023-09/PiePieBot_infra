# PiePieBot_infra
PiePieBot Infra repository

Описание ДЗ №3

1. Создание ВМ на YC
bastion_IP = 158.160.46.100
someinternalhost_IP = 10.128.0.7
2. Для подключения к someinternalhost короткой командой
Создать файл конфигурации SSH (если отсутствует) по ~/.ssh/config
Указать в нем следующие параметры
- Host someinternalhost
- HostName 10.128.0.7
- User appuser
- IdentityFile ~/.ssh/appuser
- ProxyJump appuser@158.160.46.100
После чего подключение можно производить командой ssh someinternalhost
3. Настройка Pritunl
Развернут и настроен по адресу https://158.160.46.100/#/servers
Создана Организация test_org и тестовый пользователь test
В настройках создан Сервер для подключения c Названием 10.128.0.7
Произведено тестовое подключение с помощью клиента OpenVPN на локальном устройстве (локальная ВМ + рабочая станция)
Произведена проверка подключения к someinternalhost по внутреннему адресу 10.128.0.7
Произведена настройка валидного сертификата через Let's Encrypt и sslip.io и установка имени https://158-160-46-100.sslip.io/login (фото с телефона, потому что Kaspersky мешает)
![image](https://github.com/Otus-DevOps-2023-09/PiePieBot_infra/assets/67807001/f617ea31-dbf3-4948-a644-3c15c8204541)

Описание ДЗ №4
testapp_IP = 62.84.124.251
testapp_port = 9292
