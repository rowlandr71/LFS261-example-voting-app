FROM maven:3.8.5-jdk-8-slim

WORKDIR /app 

COPY . . 

RUN mvn compile && \
    mvn package && \
    mv target/worker-jar-with-dependencies.jar /run/worker.jar && \
    rm -rf /app/*
    
EXPOSE 4000

CMD java -jar /run/worker.jar