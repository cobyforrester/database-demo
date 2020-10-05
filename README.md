# database-demo

Source code for the post: Run MySQL on Docker and use in your Java App

https://dev.to/sandrogiacom/run-mysql-on-docker-and-use-in-your-java-app-jpn


DOCKER MYSQL:
docker run --name mysql57 -p 3306:3306 \
-e MYSQL_ROOT_PASSWORD=1234 \
-e MYSQL_USER=demo_java \
-e MYSQL_PASSWORD=1234 \
-e MYSQL_DATABASE=hello_java \
-d mysql/mysql-server:5.7

RUN SPRING BOOT APP:
mvn spring-boot:run # will build first then run, MYSQL must be up and running

CHECK MYSQL DB:
docker exec -it mysql57 bash
mysql -h localhost -u root -p #password: 1234
use hello_java;
SELECT * FROM person;