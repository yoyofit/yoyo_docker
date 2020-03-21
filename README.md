# Серверная конфигурация yoyo.fit

Данный репозиторий используется для разворачивания на серверах Linux.

### Зависимости

Предварительно на сервере должны быть установлены следующие приложени:

- git
- curl
- Docker
- docker-compose

> docker-compose предпочтительно должен выполняться без привилегий суперпользователя.

### Настройка и запуск

**Авторизуйтесь на GitHub Docker Repository:**

```bash
$ cat ~/TOKEN.txt | docker login docker.pkg.github.com -u USERNAME --password-stdin
``` 

В файле `~/TOKEN.txt` должен быть персональный GitHub токен. Вместо `USERNAME` указать логин на GitHub.

**Клонируйте данный репозиторий:**

```bash
$ git clone https://github.com/yoyofit/yoyo_docker.git yoyo.fit
$ cd yoyo.fit
```

**Настройте параметры окружения:**

```bash
$ cp example.env .env
$ vi .env
```

**Инициализируйте сервер:**

```bash
$ ./appctrl init
```

**Запустите сервер:**

```bash
$ docker-compose up -d
```

PROFIT!

### Обновление сервера

...
