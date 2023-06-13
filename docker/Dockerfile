FROM ubuntu
RUN mkdir -p test
RUN apt-get update 
RUN apt-get -y upgrade 
# RUN apt update
# Add OpenJDK PPA
RUN apt install -y software-properties-common && \
    add-apt-repository ppa:openjdk-r/ppa    
# Install OpenJDK 17
RUN apt install -y openjdk-17-jdk openjdk-17-jre
COPY ./spring-petclinic-3.1.0-SNAPSHOT.jar /test/spring-petclinic-3.1.0-SNAPSHOT.jar
CMD ["java","-jar","/test/spring-petclinic-3.1.0-SNAPSHOT.jar"]
