FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    git \
    openssh-server \
    openssh-client \
    sudo \
    curl \
    wget \
    build-essential \
    python3

RUN mkdir -p /run/sshd

RUN useradd -m -s /bin/bash vscode && \
    echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN mkdir -p /home/vscode/v8 && chown -R vscode:vscode /home/vscode

WORKDIR /home/vscode

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]