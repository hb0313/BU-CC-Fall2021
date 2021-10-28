#Pull ubuntu base image
FROM ubuntu:18.04

# Install MongoDB.
RUN apt update; apt install -y gnupg2
RUN apt install -y software-properties-common
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
RUN echo 'deb https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse' > /etc/apt/sources.list.d/mongodb.list
RUN apt-get update
RUN apt-get install -y mongodb-org
RUN rm -rf /var/lib/apt/lists/*

#Create a volume
VOLUME ["/data/db"]

#Declare working directory
WORKDIR /data

#Default command 
CMD ["mongod"]

#Expose port
EXPOSE 27017
