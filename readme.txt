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

Cloning a repo from someone else's Github and pushing it to a repo on my Github
https://stackoverflow.com/questions/18200248/cloning-a-repo-from-someone-elses-github-and-pushing-it-to-a-repo-on-my-github
1. go into D:\IdeaProjects\spring-boot-docker
git remote set-url origin https://github.com/Iseehear-dw/spring-boot-docker.git


2.
git push -u origin master
