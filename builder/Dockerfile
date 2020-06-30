FROM maven:3.6.3-openjdk-8

RUN apt update && apt install -y \
    git \
    maven

# Clear cache
RUN apt-get clean

WORKDIR git

RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git && cd App42PaaS-Java-MySQL-Sample && ./mvn install -am -T 1C

RUN cp ./target/*.war /build