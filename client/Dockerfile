FROM cefore/base
WORKDIR /client
RUN apt-get update && apt-get install -y iproute2 iputils-ping iperf3
RUN cefnetdstart
# RUN cefroute add ccnx:/BitTorrent udp 10.0.2.102
