#This sets the **base image** for your Docker container.
#You're using the **Eclipse Temurin OpenJDK 21**, which is a production-grade Java runtime.
#Think of it as: "Start from a clean machine that already has Java 21 installed."
FROM eclipse-temurin:21
#Typically used to specify who maintains the Dockerfile or project.
LABEL maintainer="aniruddho.mitra.6@gmail.com"

#the below line means whenever we run the container an 'app' directory will be created in the container
#All the following instructions (like `COPY`, `ENTRYPOINT`) will run **inside** this `/app` folder.
WORKDIR /app

#the below line is for copying the source file in our local system to the mentioned directory in the container
COPY target/currency-exchange-service-0.0.12-SNAPSHOT.jar /app/currency-exchange-service-0.0.12-SNAPSHOT.jar

#This defines the **command to run when the container starts**.
 #
 #> So when you run `docker run`, it will do:
 #```bash
 #java -jar currency-exchange-service-0.0.12-SNAPSHOT.jar
ENTRYPOINT ["java","-jar","currency-exchange-service-0.0.12-SNAPSHOT.jar"]