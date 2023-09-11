# 1. Создание и настройка ВМ

### Создаю две виртуальные машины в двух разных зонах доступности: 
![Снимок экрана (92)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/4e1edd19-0991-49d5-8cc5-d8a3c4ddba43)
### Устанавливаю сервер nginx, а также билд сайта на обеих вм, проверяю:
- [Публичный адрес vm-1](http://51.250.85.112)

![Снимок экрана (99)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/c62d0940-3f2c-469f-8631-12b757b8495f)
- [Публичный адрес vm-2](http://158.160.12.119)

![Снимок экрана (100)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/a304b7ad-31d7-4de7-a451-5f3d937be6aa)

### Создаю целевую группу(target group) с включением vm-1 и vm-2:

![Снимок экрана (93)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/61225c99-079a-4a70-bac4-cf881f895170)
### Следующим этапом создаю и настраиваю группу бэкэнда(backend group):

![Снимок экрана (94)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/df3f979e-95fc-489e-8bca-a04295a1d235)
### Далее - http роутер(HTTP router):

![Снимок экрана (95)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/2db111d7-1f13-47d5-a381-38cc5fc3c7a7)
### Создаю и настраиваю балансировщик(Application load balancer):

![Снимок экрана (96)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/6113d7f1-02fc-4448-9701-ee139f0310cf)
### Тестирую работоспособность сайта: [балансировщик](http://158.160.109.82)

![Снимок экрана (98)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/2c7bb1a0-d6dd-475d-8c5e-1fb634813430)

# 2. Установка и настройка Zabbix

### Устанавливаю и настраиваю Zabbix как указано в официальной документации, проверяю сервер, веб-интерфейс, и агент:

![Снимок экрана (101)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/d0bb874b-1bc4-4ec6-b149-1334d2f89dc0)
![Снимок экрана (102)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/12653398-0ce9-4b43-96eb-2f636d07ab11)

### Устанавливаю и настраиваю Zabbix агент на Vm-1 и Vm-2, проверяю статус:
- Vm-1

![Снимок экрана (104)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/5555c620-a65b-4af7-ba9e-112c97c140f7)
  
- Vm-2

![Снимок экрана (103)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/7d217832-c320-4e6b-b641-a8e64463b831)

### Затем подключаю агенты Vm-1 и Vm-2 к Zabbix-серверу:

![Снимок экрана (240)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/43d9a4c9-567a-410c-8412-5981886be3ef)

### Настраиваю дашборды, создаю страницу system и network:

 - System

![Снимок экрана (241)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/ce10b049-8b6c-429d-b3fd-f40e02bb5fc3)

 - Network 

![Снимок экрана (242)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/63e0907a-b6ce-454d-93dc-12380c4e75fc)

# 3. Отправка логов

### Создаю ВМ для установки Elasticsearch:

![Снимок экрана (243)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/531b5834-4087-4368-9740-c1f7e25792b8)

### Устанавливаю и настраиваю Elasticsearch, проверяю:

![Снимок экрана (244)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/9423c6a9-ff21-48b4-8499-c65e7eb9d52c)

### Создаю ВМ для установки Kibana:

![Снимок экрана (243)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/1c4e2655-a7d4-49ef-87c2-26312608e692)

### Устанавливаю и настраиваю Kibana, проверяю:

![Снимок экрана (246)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/7bef18fd-c678-4fbb-9bd3-6a647875bd4f)

### Проверяю кластер Elasticsearch в Kibana:

![Снимок экрана (247)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/d1b76114-3f00-498d-aa46-fd9b9adc8f3d)
