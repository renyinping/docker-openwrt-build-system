FROM yinping/obs:buster

USER openwrt

RUN sudo chmod 777 /opt &&\
    git init /opt/openwrt &&\
    cd /opt/openwrt &&\
    git remote add origin https://git.openwrt.org/openwrt/openwrt.git &&\
    git pull &&\
    ./scripts/feeds update -a &&\
    ./scripts/feeds install -a &&\
    make download

WORKDIR /opt/openwrt
