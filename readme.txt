in powershell run like this

## Use to run mysql db docker image
docker run --name mysqldb -p 3306:3306 -e MYSQL_DATABASE=pageviewservice -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -d mysql

## Use to run RabbitMQ
docker run --name rabbitmq -p 5671:5671 -p 5672:5672 -d rabbitmq

#in powershell use backtick, in linux use \
docker run --name pageviewservice -p 8081:8081 `
--link rabbitmq:rabbitmq `
--link mysqldb:mysqldb `
-e SPRING_DATASOURCE_URL=jdbc:mysql://mysqldb:3306/pageviewservice `
-e SPRING_PROFILES_ACTIVE=mysql `
-e SPRING_RABBITMQ_HOST=rabbitmq `
springframeworkguru/pageviewservice




docker container stop $(docker container ls -aq)

docker container rm -f $(docker container ls -aq)

docker image rm -f $(docker image ls -aq)

this will build dtw/springbootdocker-container-orchestration image
mvn clean package docker:build

run, not working, need to come back
mvn docker:run


