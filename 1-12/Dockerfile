FROM centos/nginx-112-centos7

USER root

# Install PHP
RUN yum install -y centos-release-scl && \
    INSTALL_PKGS="rh-php71-php-cli rh-php71-php-common rh-php71-php-zip rh-php71-runtime" && \
    yum install -y --setopt=tsflags=nodocs $INSTALL_PKGS --nogpgcheck && \
    rpm -V $INSTALL_PKGS && \
    yum clean all -y

ENV SCL_ENABLED=rh-php71

USER 1001