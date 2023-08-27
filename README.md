# CONTL5

1. Установка Docker Compose

sudo apt update
sudo apt install docker-compose


2. Создаем файл docker-compose.yml

   nano docker-compose.yml
   
version: "3.9"
services:
  db:
    image: mariadb:10.10.2
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: 123
  adminer:
    image: mariadb:10.10.2
    restart: always
    ports:
      - "6080:8080"


3. Запускаем сервис

docker-compose up -d

4. Проверяем загруженные сервисы

docker-compose ps

5. Для прооверки доступности сервиса можно использовать команду curl:


curl http://localhost


Если все настроено правильно, вы должны увидеть HTML-код страницы приветствия сервисов. Если вы используете виртуальную машину, необходимо убедиться, что порт 80 проброшен на хостовую машину. Если вы используете Docker Desktop для Windows или Mac, то доступ к контейнерам осуществляется через виртуальную сеть, поэтому вместо localhost необходимо использовать IP-адрес виртуальной машины Docker.

![L5_1](https://github.com/PavelE13/CONTL5/assets/94640966/d8fe9a0d-c38a-4742-9779-94aa2a43f75b)
![L5_2](https://github.com/PavelE13/CONTL5/assets/94640966/2d3ac4c3-ce1e-48b9-8c50-5cabb19a83c8)
![L5_3](https://github.com/PavelE13/CONTL5/assets/94640966/5ed77ab0-2f1a-44a2-9ed7-eb481be379e2)

