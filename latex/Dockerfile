From debian
LABEL maintainer="Cyris Tseng"

RUN apt update \
    && apt install -y openssh-server wget make git\
    && mkdir /var/run/sshd \
    && sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config \
    && sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config \
    && sed -i 's/#PubkeyAuthentication yes/PubkeyAuthentication yes/' /etc/ssh/sshd_config \
    && sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config \
    && echo 'root:latex' | chpasswd

RUN apt install -y texlive-base texlive-bibtex-extra texlive-fonts-recommended texlive-fonts-extra texlive-latex-extra texlive-latex-recommended latex-cjk-all

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
