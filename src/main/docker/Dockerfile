FROM openjdk

#ARG JAR_FILE=*.jar
ARG JAR_FILE=maven/${project.build.finalName}.jar
COPY ${JAR_FILE} app.jar

#another way
#ADD maven/${project.build.finalName}.jar app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
