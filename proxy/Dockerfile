FROM cefore/base
WORKDIR /proxy
RUN apt-get update && apt-get install -y iproute2 iputils-ping iperf3
RUN cefnetdstart

CMD tc qdisc add dev eth0 root handle 1:0 tbf rate 100mbit burst 50kb limit 100kb \
    && tc qdisc add dev eth0 parent 1:1 handle 10:1 netem delay 10ms \
    && tc qdisc add dev eth1 root handle 1:0 tbf rate 100mbit burst 50kb limit 100kb \
    && tc qdisc add dev eth1 parent 1:1 handle 10:1 netem delay 10ms \

