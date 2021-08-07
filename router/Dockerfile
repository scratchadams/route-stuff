FROM handsonsecurity/seed-server:bgp
ARG BIRD_CONF

RUN echo ${BIRD_CONF}
#Copy the bird config file
COPY ${BIRD_CONF} /etc/bird/bird.conf

#Delete the default routing entry and start BGP server
CMD ip route del default ; mkdir -p /run/bird && bird -d
