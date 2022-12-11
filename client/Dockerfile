FROM cefore/base
WORKDIR /client
RUN apt-get update && apt-get install -y iproute2 iputils-ping iperf3
RUN cefnetdstart

CMD cefroute add ccnx:/BitTorrent udp 10.0.2.102 \
    && tc qdisc add dev eth0 root handle 1:0 tbf rate 100mbit burst 50kb limit 100kb

