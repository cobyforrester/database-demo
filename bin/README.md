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