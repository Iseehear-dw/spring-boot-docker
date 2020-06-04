1.
mvn clean package docker:build docker:run

2. start in background
mvn clean package docker:build docker:start

3. stop,also remove container
mvn docker:stop
