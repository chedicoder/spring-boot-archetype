FROM openjdk:17-jdk-alpine

VOLUME /tmp

COPY /target/libs /usr/local/pod/libs
ARG JAR_FILE=/target/contract-service.jar
COPY ${JAR_FILE} /usr/local/pod/
COPY ./trusted-certs/ca.crt /tmp

# Import the certificate into the Java truststore
RUN keytool -importcert \
    -cacerts \
    -file /tmp/ca.crt \
    -alias msic-dev-root-cert \
    -storepass changeit -noprompt
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-Duser.timezone=Africa/Casablanca","-jar","/usr/local/pod/contract-service.jar"]

