FROM maven:3.6.3-openjdk-8

RUN apt update && apt install -y \
    git

WORKDIR git

RUN git clone https://github.com/enfurec1do/App42PaaS-Java-MySQL-Sample.git && cd App42PaaS-Java-MySQL-Sample && mvn clean && mvn install

RUN cp ./target/*.war /build && cp ./WebContent/Config.properties /build