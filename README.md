#### Using Docker to test this app.

```bash
### Compile Test Jar Code
docker run --rm -it -p 9010:8081 -u gradle -v $(pwd):/home/gradle/project -w /home/gradle/project gradle gradle clean build


### Run Jar
docker run --rm -it -p 9010:8081 -u gradle -v $(pwd):/home/gradle/project -w /home/gradle/project gradle gradle bootRun



* curl -X GET 'http://localhost:9010/rest/mscovid/test?msg=testing'