FROM alpine

# maintainer details
MAINTAINER Steve HOUEL "steve.houel@thalesgroup.com"

# update packages and install maven
RUN  apt-get update && apt-get install -y git && apt-get clean

# Declare working directory to current dir
WORKDIR /app

# run terminal
ENTRYPOINT["git"]
CMD ["--version]
