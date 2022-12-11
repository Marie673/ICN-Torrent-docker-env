FROM queeno/ubuntu-desktop
WORKDIR /producer

RUN apt-get update && apt-get install -y iproute2 iputils-ping iperf3
RUN apt-get install -y qbittorrent

CMD tc qdisc add dev eth0 root handle 1:0 tbf rate 100mbit burst 50kb limit 100kb