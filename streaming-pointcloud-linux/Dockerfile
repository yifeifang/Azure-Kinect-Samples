FROM ubuntu:18.04

RUN apt-get update && \
    apt-get install -y wget && \
    wget https://packages.microsoft.com/ubuntu/18.04/prod/pool/main/libk/libk4a1.4/libk4a1.4_1.4.1_amd64.deb && \
    wget https://packages.microsoft.com/ubuntu/18.04/prod/pool/main/libk/libk4a1.4-dev/libk4a1.4-dev_1.4.1_amd64.deb && \   
    apt-get install -y ./libk4a1.4_1.4.1_amd64.deb && \
    apt-get install -y ./libk4a1.4-dev_1.4.1_amd64.deb && \
    rm ./libk4a1.4_1.4.1_amd64.deb && \
    rm ./libk4a1.4_1.4.1_amd64.deb
