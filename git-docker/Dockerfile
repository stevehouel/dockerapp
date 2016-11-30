FROM ubuntu:16.04

# maintainer details
MAINTAINER Steve HOUEL "steve.houel.pro@gmail.com"

# update packages and install maven
RUN  apt-get update && apt-get install -y git && apt-get clean

# Declare working directory to current dir
WORKDIR /app

# run terminal
ENTRYPOINT["git"]
CMD ["--version]
