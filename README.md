# Docker Application

What I mean with Docker Application is docker container that can be run one time to execute an action and then shutdown.

With that kind off image, no need for you to install libraries / dependencies with many kind of version. You only need to run the docker container and execute your command.

## Available Application


### Git
### Maven
### Ansible
### Python

## Alias
For a better use of those container, you can create alias on your machine and then use them as if you had install the real application.
By default all alias map current directory, so you only need to run command where you want

Example :

```
mvn
```

It will execute maven container and launch the default command who is --version

Otherwise you can do

```
mvn clean install
```

This will override default docker command and run clean install goals

### Maven
alias mvn="docker run -d --rm -v $(pwd):/app $(YOUR_IMAGE_NAME):$(VERISON_TO_USE)"

### Ansible
alias ansible-playbook="docker run -d --rm -v $(pwd):/app ansible:2.1.1.0"
