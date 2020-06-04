build docker iamge
mvn clean package docker:build

run docker iamge
docker run -p 8080:8080 -d dtw2005/springbootdocker

push to docker hub public repository
1.
~/.m2/settings.xml
    <servers>
        <server>
            <id>docker-hub</id>
            <username>dtw2005</username>
            <password>your-password</password>
        </server>
    </servers>
2.
mvn clean install docker:build docker:push

