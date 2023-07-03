FROM ubuntu:18.04
# Setting up Linux Software Repository for Microsoft Products 
# Ref: https://learn.microsoft.com/en-us/windows-server/administration/linux-package-repository-for-microsoft-software
RUN apt update && \
    apt install -y curl && \
    apt install -y gnupg && \
    apt install -y software-properties-common && \
    apt install -y xauth && \
    curl -sSL https://packages.microsoft.com/keys/microsoft.asc | apt-key add - && \
    apt-add-repository https://packages.microsoft.com/ubuntu/18.04/prod && \
    apt-add-repository ppa:mosquitto-dev/mosquitto-ppa && \
    rm -rf /var/lib/apt/lists/*

RUN apt update && \
    ACCEPT_EULA=Y apt install -y libk4a1.4 && \
    ACCEPT_EULA=Y apt install -y libk4a1.4-dev && \
    ACCEPT_EULA=Y apt install -y k4a-tools && \
    apt install -y mosquitto-dev && \
    apt install -y build-essential && \
    apt install -y libeigen3-dev && \
    apt install -y gdb && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir -p /etc/udev/rules.d/
COPY ./docker_resource/99-k4a.rules /etc/udev/rules.d/
RUN chmod a+rwx /etc/udev/rules.d
