# OS
FROM ubuntu
# metadata
LABEL Description="Devops 101" Version="1.0"
# paquetes necesarios
RUN apt-get update && apt-get install -y \
    graphite-carbon
# el puerto que necesita graphite 
EXPOSE 2003
# donde dejar la data
VOLUME /var/lib/graphite/whisper
# --nodaemon 
ENTRYPOINT /usr/bin/carbon-cache --config /etc/carbon/carbon.conf --nodaemon start
