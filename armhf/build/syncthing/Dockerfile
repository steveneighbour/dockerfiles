FROM casept/alpine-armhf:edge 

#Syncthing version
ENV ST_VERSION="0.14.9"
#Processor architecture
ENV ST_ARCH="armhf"

COPY install.sh /usr/local/bin/
RUN install.sh && rm /usr/local/bin/install.sh
USER syncthing
ENTRYPOINT ["dumb-init", "syncthing", "-gui-address", "0.0.0.0:8384", "-no-browser"]
