FROM jacklul/pihole:latest
RUN apt update && apt install -y unbound

COPY lighttpd-external.conf /etc/lighttpd/external.conf 
COPY unbound-pihole.conf /etc/unbound/unbound.conf.d/pi-hole.conf
COPY install_unbound_and_s6_init.sh install_unbound_and_s6_init.sh

RUN chmod +x install_unbound_and_s6_init.sh
ENTRYPOINT ./install_unbound_and_s6_init.sh
