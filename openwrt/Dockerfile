FROM yinping/obs:buster

USER openwrt

RUN sudo chmod 777 /opt &&\
    git init /opt/openwrt &&\
    cd /opt/openwrt &&\
    git remote add origin https://git.openwrt.org/openwrt/openwrt.git 

RUN git pull 
RUN ./scripts/feeds update -a 
RUN ./scripts/feeds install -a 
RUN make download

WORKDIR /opt/openwrt
