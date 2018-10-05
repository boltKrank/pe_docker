FROM centos:centos7

RUN yum -y update; yum clean all
RUN yum -y install openssh-server passwd; yum clean all
ADD ./start.sh /start.sh
RUN mkdir /var/run/sshd

RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N '' 

RUN chmod 755 /start.sh
# EXPOSE 22
RUN ./start.sh

# Make sudo work
ARG SUDO_USER=puppet
ARG SUDO_USER_PASS=puppetlabs
RUN yum install sudo -y && \
    useradd -g wheel ${SUDO_USER} && \
    echo "${SUDO_USER}:${SUDO_USER_PASS}" | chpasswd && \
    sed -i -e 's/^\(%wheel\s\+.\+\)/#\1/gi' /etc/sudoers && \
    echo -e '\n%wheel ALL=(ALL) ALL' >> /etc/sudoers && \
    echo -e '\nDefaults:root   !requiretty' >> /etc/sudoers && \
    echo -e '\nDefaults:%wheel !requiretty' >> /etc/sudoers

ENTRYPOINT ["/usr/sbin/sshd", "-D"]
