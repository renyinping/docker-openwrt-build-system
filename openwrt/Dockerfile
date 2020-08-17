FROM yinping/obs:buster

USER openwrt
WORKDIR /opt

RUN git clone https://git.openwrt.org/openwrt/openwrt.git

WORKDIR /opt/openwrt

RUN ./scripts/feeds update -a &&\
    ./scripts/feeds install -a &&\
    make download
