# 1. Создание и настройка ВМ

### 1.1 - Создаю две виртуальные машины в двух разных зонах доступности: 
![Снимок экрана (92)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/4e1edd19-0991-49d5-8cc5-d8a3c4ddba43)
### Устанавливаю сервер nginx, а также билд сайта на обеих вм, проверяю:
- [Публичный адрес vm-1](http://51.250.85.112)

![Снимок экрана (99)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/c62d0940-3f2c-469f-8631-12b757b8495f)
- [Публичный адрес vm-2](http://158.160.12.119)

![Снимок экрана (100)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/a304b7ad-31d7-4de7-a451-5f3d937be6aa)

### 1.2 - Создаю целевую группу(target group) с включением vm-1 и vm-2:

![Снимок экрана (93)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/61225c99-079a-4a70-bac4-cf881f895170)
### 1.3 - Следующим этапом создаю и настраиваю группу бэкэнда(backend group):

![Снимок экрана (94)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/df3f979e-95fc-489e-8bca-a04295a1d235)
### 1.4 - Далее - http роутер(HTTP router):

![Снимок экрана (95)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/2db111d7-1f13-47d5-a381-38cc5fc3c7a7)
### 1.5 - Создаю и настраиваю балансировщик(Application load balancer):

![Снимок экрана (96)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/6113d7f1-02fc-4448-9701-ee139f0310cf)
### 1.6 - Тестирую работоспособность сайта: [балансировщик](http://158.160.109.82)

![Снимок экрана (98)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/2c7bb1a0-d6dd-475d-8c5e-1fb634813430)

# 2. Установка и настройка Zabbix

### 2.1 - Устанавливаю и настраиваю Zabbix как указано в официальной документации, проверяю сервер, веб-интерфейс, и агент:

![Снимок экрана (101)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/d0bb874b-1bc4-4ec6-b149-1334d2f89dc0)
![Снимок экрана (102)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/12653398-0ce9-4b43-96eb-2f636d07ab11)

### 2.2 - Устанавливаю и настраиваю Zabbix агент на Vm-1 и Vm-2, проверяю статус:
- Vm-1

![Снимок экрана (104)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/5555c620-a65b-4af7-ba9e-112c97c140f7)
  
- Vm-2

![Снимок экрана (103)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/7d217832-c320-4e6b-b641-a8e64463b831)

### 2.3 - Затем подключаю агенты Vm-1 и Vm-2 к Zabbix-серверу:

 - Логин и пароль Zabbix: **Admin zabbix**

![Снимок экрана (240)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/43d9a4c9-567a-410c-8412-5981886be3ef)

### 2.4 - Настраиваю дашборды, создаю страницу system и network:

 - System

![Снимок экрана (241)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/ce10b049-8b6c-429d-b3fd-f40e02bb5fc3)

 - Network 

![Снимок экрана (242)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/63e0907a-b6ce-454d-93dc-12380c4e75fc)

# 3. Отправка логов

### 3.1 - Создаю ВМ для установки Elasticsearch:

![Снимок экрана (243)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/531b5834-4087-4368-9740-c1f7e25792b8)

### 3.2 - Устанавливаю и настраиваю Elasticsearch, проверяю:

![Снимок экрана (244)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/9423c6a9-ff21-48b4-8499-c65e7eb9d52c)

### 3.3 - Создаю ВМ для установки Kibana:

 - Логин и пароль Kibana: **elastic vkShZ8RVk6W2Mn9yGJil**

![Снимок экрана (243)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/1c4e2655-a7d4-49ef-87c2-26312608e692)

### 3.4 - Устанавливаю и настраиваю Kibana, проверяю:

![Снимок экрана (246)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/7bef18fd-c678-4fbb-9bd3-6a647875bd4f)

### 3.5 - Проверяю кластер Elasticsearch в Kibana:

![Снимок экрана (247)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/d1b76114-3f00-498d-aa46-fd9b9adc8f3d)

### 3.6 - Устанавливаю и настраиваю filebeat(vm-1 и vm-2) на отправку логов в Elasticsearch, проверяю в Kibana:

![Снимок экрана (248)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/61f89516-45af-4066-8ade-54e2b4c5f8d1)

![Снимок экрана (249)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/0b4a6ced-12b3-4135-a374-104a160dc11d)

### 3.7 - Логи Elasticsearch:

![Снимок экрана (253)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/5383c1ba-83f3-458f-935c-783a0a28623e)

# 4. Сеть

### 4.1 - Создаю группы безопасности:

 - входящий:

![Снимок экрана (254)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/c418e28e-cfcc-4a58-80b6-78709ce4cf90)


 - исходящий:

![Снимок экрана (255)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/c72f2e02-9320-40ab-ac49-b88ad078ee63)


# 5. Создание snapshot

### 5.1 - Создаю снимки дисков всех ВМ:

![Снимок экрана (252)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/56a1360e-0017-4d0e-85ec-8f04ae22ba71)

### 5.2 - Произвожу настройку snapshot(ежедневное копирование, срок жизни - одна неделя):

![Снимок экрана (250)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/5a9afae9-cffd-4119-931f-b712db599621)

### 5.3 - Сохраняю настройки:

![Снимок экрана (251)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/42a8ffa4-34cb-4a78-bde5-a40158cdb8c9)

