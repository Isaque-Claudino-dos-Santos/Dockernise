FROM ubuntu:24.04

ENV JAVA_HOME=/lib/jvm/jdk-24.0.1-oracle-x64

COPY . /usr/src/app

WORKDIR /usr/src/app

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y curl

# -- Install Maven -- #
RUN apt-get install -y maven

# -- Install Java -- #
RUN curl -O https://download.oracle.com/java/24/latest/jdk-24_linux-x64_bin.deb
RUN apt-get install -y ./jdk-24_linux-x64_bin.deb

RUN mvn install

CMD ["mvn", "initialize"]
