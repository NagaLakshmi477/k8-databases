FROM almalinux:9

RUN dnf install -y telnet net-tools iputils \
    && dnf clean all
RUN useradd roboshop
USER roboshop
CMD ["sleep","100000"]