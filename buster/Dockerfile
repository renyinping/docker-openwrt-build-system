FROM debian:buster

RUN apt-get update &&\
    apt-get install -y asciidoc bash binutils bzip2 flex git-core \
        g++ gcc util-linux gawk help2man intltool libelf-dev zlib1g-dev \
        make libncurses5-dev libssl-dev patch perl-modules python2-dev \
        unzip wget gettext xsltproc zlib1g-dev libboost-all-dev \
        libxml-parser-perl libusb-dev bin86 bcc sharutils openjdk-11-jdk \
        subversion g++ zlib1g-dev build-essential git python python3 \
        python3-distutils libncurses5-dev gawk gettext unzip file \
        libssl-dev wget libelf-dev ecj fastjar java-propose-classpath \
        ccache bash sudo curl &&\
    apt-get autoclean &&\
    useradd -s /bin/bash -m openwrt &&\
    echo 'openwrt ALL=NOPASSWD: ALL' > /etc/sudoers.d/openwrt &&\
    curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o /home/openwrt/.git-completion.bash &&\
    echo . >> /home/openwrt/.profile &&\
    echo 'if [ -f ~/.git-completion.bash ]; then' >> /home/openwrt/.profile &&\
    echo '. ~/.git-completion.bash' >> /home/openwrt/.profile &&\
    echo 'fi' >> /home/openwrt/.profile

USER openwrt
WORKDIR /opt
