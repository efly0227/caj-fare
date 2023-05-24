## Fare
* Swagger UI
```
http://${DOMAIN}/swagger-ui.html
```

* Test
```bash=
./gradlew clean test --info
```

* Code Scan
```bash=
./gradlew sonarqube \
  -Dsonar.host.url=${SONARQUBE_URL} \
  -Dsonar.login=${USER} \
  -Dsonar.password=${PASSWORD} \
  -Dsonar.projectName=fare-${STUDENT_ID} \
  -Dsonar.projectKey=fare-${STUDENT_ID} 
```

* Build Artifact
```bash=
./gradlew clean build
```

* Build Image (COPY Artifact into image)
```bash=
docker build -f Dockerfile-openjdk -t fare:latest .
```

* Build Image (Gradle build in image)
```bash=
docker build -f Dockerfile-gradle -t fare:latest .
```

<<<<<<< HEAD
* Run image 20230524005
=======
* Run image 1234
>>>>>>> 5a311217de9e86e07c1001ba6a3eac44664b0c0e
```bash=
# default port 8080
docker run -p 8080:8080 fare:latest
```
