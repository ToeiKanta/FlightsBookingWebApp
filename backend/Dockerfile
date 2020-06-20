FROM openjdk:8

COPY . /backend
WORKDIR /backend

run ./gradlew -no-daemon bootJar

# stage 1

FROM openjdk:8

COPY --from=0 /backend/build/libs/team24-0.0.1-SNAPSHOT.jar /app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
