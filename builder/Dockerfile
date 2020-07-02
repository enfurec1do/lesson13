FROM maven:3.6.3-openjdk-8

RUN apt update && apt install -y \
    git

RUN git clone https://github.com/enfurec1do/App42PaaS-Java-MySQL-Sample.git && cd App42PaaS-Java-MySQL-Sample && mvn clean && mvn install

WORKDIR App42PaaS-Java-MySQL-Sample

RUN cp WebContent/Config.properties target/Config.properties
