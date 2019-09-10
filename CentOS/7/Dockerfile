FROM centos:centos7 AS afcentos7
LABEL "maintainer"="Andrew J. Huffman" \
      "maintainer_email"="huffy@redhat.com"

RUN ["/bin/bash", "-c", "yum update -y"]
RUN ["/bin/bash", "-c", "yum install -y epel-release centos-release-scl"]
RUN ["/bin/bash", "-c", "yum install -y ansible"]
RUN ["/bin/bash", "-c", "yum clean all"]
RUN ["/bin/bash", "-c", "rm -rf /var/cache/*"]

CMD ["/bin/bash"]
