# development notices
- test VM ip: 192.168.56.49 (cicd_test_49)

# Instructions, installing from CLI (on CentOS 7)

## Docker
- Getting help: [Install Docker on CentOS 7](https://linuxize.com/post/how-to-install-and-use-docker-on-centos-7/).
- Install steps:
~~~
(sudo) yum update -y
(sudo) yum install yum-utils device-mapper-persistent-data lvm2
(sudo) yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
(sudo) yum install docker-ce
(sudo) systemctl start docker
(sudo) systemctl enable docker
(sudo) systemctl status docker
docker -v
~~~

## Install !!! Git !!!
## Install !!! Docker compose !!!
~~~
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
docker-compose up
~~~

## Work with Jenkins's Docker image
- Getting help: [Jenkins Docker image](https://hub.docker.com/r/jenkins/jenkins).
- Hint: admin / 000000
~~~
docker pull jenkins/jenkins:lts
docker run -p 8080:8080 -p 50000:50000 jenkins
docker exec -it <conatiner_name> bash
~~~

## Work with apache's Docker image
- Getting help: [apache Docker image](https://hub.docker.com/_/httpd/).
- Hint: index file path: /usr/local/apache2/htdocs/index.html
~~~
docker pull httpd
docker run -p 8080:8080 -p 50000:50000 jenkins
docker exec -it <conatiner_name> bash
~~~