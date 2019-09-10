FROM debian:bullseye AS afbullseye
LABEL "maintainer"="Andrew J. Huffman" \
      "maintainer_email"="huffy@redhat.com"

RUN ["/bin/bash", "-c", "apt-get update"]
RUN ["/bin/bash", "-c", "apt-get upgrade -y"]
RUN ["/bin/bash", "-c", "apt-get install -y python-pip acl"]
RUN ["/bin/bash", "-c", "pip install ansible jmespath"]
RUN ["/bin/bash", "-c", "apt-get clean"]
RUN ["/bin/bash", "-c", "rm -rf /var/cache/*"]

CMD ["/bin/bash"]
