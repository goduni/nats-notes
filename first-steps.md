# Первые шаги при работе с NATS.io

Для начала - стоит установить сам NATS. Рекомендую использовать **[Docker](https://https://docs.docker.com/install)** <- кликабельно.


## Docker
```
docker pull nats:latest
docker run -p 4222:4222 -ti nats:latest
```

## Пакетные менеджеры

Windows

`choco install nats-server`

MacOS

`brew install nats-server`

Linux

`yay nats-server`

## Установка из билда

1) Выбрать версию NATS **[здесь](https://github.com/nats-io/nats-server/releases/)**
2) Подставить выбранную версию сюда (заменить X, Y, Z):

```
curl -L https://github.com/nats-io/nats-server/releases/download/vX.Y.Z/nats-server-vX.Y.Z-linux-amd64.zip -o nats-server.zip
unzip nats-server.zip -d nats-server
sudo cp nats-server/nats-server-vX.Y.Z-linux-amd64/nats-server /usr/bin
```

## Установка из исходников

Требует наличия установленного Go.

```GO111MODULE=on go get github.com/nats-io/nats-server/v2```



## Запуск сервера

Для запуска сервера - достаточно написать `nats-server` в консоли. Если вы хотите включать JetStream, обязательно добавьте `-js` к команде. 
Результат будет похож на:

```
[41634] 2019/05/13 09:42:11.745919 [INF] Starting nats-server version 2.6.2
[41634] 2019/05/13 09:42:11.746240 [INF] Listening for client connections on 0.0.0.0:4222
...
[41634] 2019/05/13 09:42:11.746249 [INF] Server id is NBNYNR4ZNTH4N2UQKSAAKBAFLDV3PZO4OUYONSUIQASTQT7BT4ZF6WX7
[41634] 2019/05/13 09:42:11.746252 [INF] Server is ready
```
