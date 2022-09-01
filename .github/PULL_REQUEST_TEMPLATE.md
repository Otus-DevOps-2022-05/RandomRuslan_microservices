# Выполнено ДЗ № 16
 - [*] Основное ДЗ: изучил основы по образам и контейнерам

## В процессе сделано:
1. Изучил образы и контейнеры докера
2. Развернул докер на удаленном сервере с помощью docker-machine
3. Загрузил образ приложения на docker hub, использовал загруженный образ для локальной розвертки

## Как запустить проект:
```shell
docker run --name reddit -d -p 9292:9292 wrkrus/otus-reddit:1.0
```

## Как проверить работоспособность:
Открыть приложение в браузере: `<Внешний ip сервиса>:9292`