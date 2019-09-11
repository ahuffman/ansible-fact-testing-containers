FROM centos:centos7 AS afcentos7
LABEL "maintainer"="Andrew J. Huffman" \
      "maintainer_email"="huffy@redhat.com"

RUN ["/bin/bash", "-c", "yum update -y"]
RUN ["/bin/bash", "-c", "yum install -y epel-release centos-release-scl"]
RUN ["/bin/bash", "-c", "yum install -y ansible sudo"]
RUN ["/bin/bash", "-c", "yum clean all"]
RUN ["/bin/bash", "-c", "rm -rf /var/cache/*"]
RUN ["/bin/bash", "-c", "useradd -U -u 2000 -c \"Travis CI User\" -s /bin/bash -p \"!$6$2v7PYfJS$Dhw47WXCUx/g7aqkyO1Ieqf/kLOVEoEgqtKaOrAzQ/3ivQb6/kfQd/NW3UI4C8UmlK6L5XcMibzLQWLQUNhH21\" -d /home/travis -m -G wheel travis"]
COPY sudoers /etc/sudoers
RUN ["/bin/bash", "-c", "chmod 440 /etc/sudoers"]

CMD ["/bin/bash"]
