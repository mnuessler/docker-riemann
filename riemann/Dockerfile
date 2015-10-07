FROM java:8

MAINTAINER Matthias Nüßer <m.nuessler@web.de>

ENV RIEMANN_VERSION 0.2.10

ADD https://aphyr.com/riemann/riemann_${RIEMANN_VERSION}_all.deb /tmp/
RUN dpkg -i /tmp/riemann_${RIEMANN_VERSION}_all.deb && \
    rm /tmp/riemann_${RIEMANN_VERSION}_all.deb

COPY riemann.config /etc/riemann/

CMD ["start"]
ENTRYPOINT ["/usr/bin/riemann"]
