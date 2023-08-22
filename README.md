# Создание и настройка ВМ

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

# Установка и настройка Zabbix

### Устанавливаю и настраиваю Zabbix как указано в официальной документации, проверяю сервер, веб-интерфейс, и агент:

![Снимок экрана (101)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/d0bb874b-1bc4-4ec6-b149-1334d2f89dc0)
![Снимок экрана (102)](https://github.com/AleksandrShirobokov/sysAdmin/assets/69298696/12653398-0ce9-4b43-96eb-2f636d07ab11)

