FROM maven:3.6.3-openjdk-8

RUN apt update && apt install -y \
    git \
    maven

WORKDIR git

RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git && cd App42PaaS-Java-MySQL-Sample && mvn clean && mvn install

RUN cp ./target/*.war /build