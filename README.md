# RandomRuslan_microservices
RandomRuslan microservices repository


# 16. Docker 2

1. Изучил образы и контейнеры докера
2. Развернул докер на удаленном сервере с помощью docker-machine
3. Загрузил образ приложения на docker hub, использовал загруженный образ для локальной развертки


# 17. Docker 3
1. Развернул 4х-компонентное приложение, где 3 приложения созданы по собственным докерфайлам.
2. Развернул это же приложение, но с установленными при запуске env-переменными и измененными алиасами:
```shell
docker run -d --network=reddit --network-alias=post_db_x  --network-alias=comment_db_x mongo:5.0
docker run -d --network=reddit --network-alias=post_x -e POST_DATABASE_HOST=post_db_x wrkrus/post:1.0
docker run -d --network=reddit --network-alias=comment_x -e COMMENT_DATABASE_HOST=comment_db_x wrkrus/comment:1.0
docker run -d --network=reddit -e POST_SERVICE_HOST=post_x -e COMMENT_SERVICE_HOST=comment_x -p 9292:9292 wrkrus/ui:1.0
```
3. Оптимизировал образ ui-модуля.
4. Подключил вольюм.


# 18. Docker 4
1. Поработал с сетями: none, host, bridge.
2. Поработал с docker-compose: сети, параметризация, работа с базовым именем проекта

Базовое имя проекта - это название рабочей директории.
Для изменения этого имени необходимо добавить в .env переменную `COMPOSE_PROJECT_NAME`.
