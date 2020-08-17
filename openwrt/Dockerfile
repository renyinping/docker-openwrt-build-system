FROM yinping/obs:buster

USER openwrt

RUN sudo chmod 777 /opt &&\
    git init /opt/openwrt &&\
    cd /opt/openwrt &&\
    git remote add origin https://git.openwrt.org/openwrt/openwrt.git 

RUN cd /opt/openwrt && git pull 
RUN cd /opt/openwrt && ./scripts/feeds update -a 
RUN cd /opt/openwrt && ./scripts/feeds install -a 
RUN cd /opt/openwrt && make download

WORKDIR /opt/openwrt
