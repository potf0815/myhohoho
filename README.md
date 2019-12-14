# myhohoho christmas cubes

A simple one-docker-container webserver

- About:
upload one to six 6 pictures, and get back a .pdf for building a "myhohoho" christmas cube to put onto your christmas tree.

- Purpose:
Docker & Cloud Computing education with some kids of Schule Fluntern, Zürich, December 2015

- Technology:
docker, git, imagemagick, perl, pdf, apache webserver, cloud

- Tools needed for the user:
colour printer + paper glue + scissor

- Time needed for one cube:
Approx. 3 minutes

# Build and run the container

clone the repository with git:

git clone https://github.com/frankrutz/myhohoho

cd myhohoho

docker build -t myhohoho .

To run the container with apache starting in daemon-mode:

docker run -p 80:80 --name hohoho -d myhohoho apachectl -D FOREGROUND

Now, you will be able to access the app at

http://youripadress/

# History
- Nov/Dec 2015:
created, build and used on Google Cloud Engine

- 22nd Jan 2017:
released on github
- 14th Dec 2019
update to httpd:2.4



# Setting up a Containerhost on Google Cloud

We run CentOS7, standard machines, http https enabled

sudo su -

yum install -y docker

yum install -y git

systemctl start docker


 
