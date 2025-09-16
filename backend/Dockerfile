FROM maven:3.8.3-openjdk-17

COPY . /opt/

WORKDIR /opt

RUN rm -rf src/main/resources/application.properties
RUN cp application.properties src/main/resources/application.properties

RUN mvn clean package -DskipTests

WORKDIR /opt/target/

EXPOSE 8080

CMD [ "java", "-jar", "student-registration-backend-0.0.1-SNAPSHOT.jar" ]
