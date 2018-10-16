FROM centos/nginx-112-centos7

USER root

# Install PHP
RUN yum install -y centos-release-scl && \
    INSTALL_PKGS="rh-php71-php" && \
    yum install -y --setopt=tsflags=nodocs $INSTALL_PKGS --nogpgcheck && \
    rpm -V $INSTALL_PKGS && \
    yum clean all -y

USER 1001