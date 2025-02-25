FROM espressif/idf:release-v5.4
RUN echo "source /opt/esp/idf/export.sh" >> /root/.bashrc
# Install Tex Live
RUN apt-get update && apt-get -y upgrade \
    && apt-get -y install --no-install-recommends python3-pip \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

RUN curl -fsSL -o get-platformio.py https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py \
    && python3 get-platformio.py \ 
    && export PATH=$PATH:$HOME/.local/bin \ 
    && mkdir -p /usr/local/bin \
    && ln -s ~/.platformio/penv/bin/platformio /usr/local/bin/platformio \
    && ln -s ~/.platformio/penv/bin/pio /usr/local/bin/pio \
    && ln -s ~/.platformio/penv/bin/piodebuggdb /usr/local/bin/piodebuggdb \