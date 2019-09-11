FROM debian:bullseye AS afbullseye
LABEL "maintainer"="Andrew J. Huffman" \
      "maintainer_email"="huffy@redhat.com"

RUN ["/bin/bash", "-c", "apt-get update"]
RUN ["/bin/bash", "-c", "apt-get upgrade -y"]
RUN ["/bin/bash", "-c", "apt-get install -y python-pip acl sudo"]
RUN ["/bin/bash", "-c", "pip install ansible jmespath"]
RUN ["/bin/bash", "-c", "apt-get clean"]
RUN ["/bin/bash", "-c", "rm -rf /var/cache/*"]
RUN ["/bin/bash", "-c", "useradd -U -u 2000 -c \"Travis CI User\" -s /bin/bash -p \"!$6$2v7PYfJS$Dhw47WXCUx/g7aqkyO1Ieqf/kLOVEoEgqtKaOrAzQ/3ivQb6/kfQd/NW3UI4C8UmlK6L5XcMibzLQWLQUNhH21\" -d /home/travis -m -G sudo travis"]
COPY sudoers /etc/sudoers
RUN ["/bin/bash", "-c", "chmod 440 /etc/sudoers"]

CMD ["/bin/bash"]
