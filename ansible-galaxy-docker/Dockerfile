FROM ubuntu:16.04

MAINTAINER Steve HOUËL <steve.houel.pro@gmail.com>

# Installing Ansible and removing as apt as possible
RUN echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" | tee /etc/apt/sources.list.d/ansible.list \
&& echo "deb-src http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" | tee -a /etc/apt/sources.list.d/ansible.list \
&& apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 7BB9C367 \
&& apt-get update -y \
&& apt-get install -y ansible \
&& rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/ansible.list \
&& echo 'localhost' > /etc/ansible/hosts

WORKDIR /app

# default command: display Ansible version
ENTRYPOINT [ "ansible-galaxy" ]
CMD [ "--version" ]
