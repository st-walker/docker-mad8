FROM centos:7

ADD https://www.desy.de/fel-beam/mad8/files/mad8DesyPublic_8.51.18.zip /

RUN yum install -y \
    libX11-devel-1.6.7 \
    compat-libgfortran-41-4.1.2 \
    unzip-6.0 \
    && yum clean all \
    && unzip mad8DesyPublic_8.51.18.zip

COPY entry-point /mad8DesyPublic/entry-point

WORKDIR /mad8DesyPublic/
ENTRYPOINT ["/mad8DesyPublic/entry-point"]

LABEL maintainer="stuart.walker@desy.de"
