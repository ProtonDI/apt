FROM debian:bullseye

RUN sed -i "s/deb.debian.org/192.168.10.108:3142/g" /etc/apt/sources.list
RUN apt-get update && \
    apt-get install --no-install-recommends -y \
        apt-transport-https ca-certificates curl gpg apt-utils && \
    curl https://protondi.github.io/apt/pubkey.gpg | gpg --dearmor -o /etc/apt/trusted.gpg.d/proxmox-release-bullseye.gpg && \
    echo "deb [signed-by=/etc/apt/trusted.gpg.d/proxmox-release-bullseye.gpg] https://protondi.github.io/apt bullseye main" > /etc/apt/sources.list.d/protondi.list && \
    apt-get update && \
    apt-get install -y proxmox-ve