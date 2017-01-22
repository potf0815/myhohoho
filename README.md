# January 2017: myhohoho is currently running on 
http://104.155.74.75/


# myhohoho christmas cubes

- About:
upload one to six 6 pictures, and get back a .pdf for building a "myhohoho" christmas cube to put onto your christmas tree.

- Purpose:
Docker & Cloud Computing education in Schule Fluntern, Zürich, December 2015

- Technology:
docker, git, imagemagick, perl, pdf, apache webserver, cloud

- Tools needed for the user:
colour printer + paper glue + scissor

- Time needed for one cube:
Approx. 3 minutes

- Tip:
good schoolclass activity to give a present to the teacher: each pupil makes a personal cube.

- Programmed by:
A container application constructed with primary school kids at Schule Fluntern in Zürich during November/December 2015.

- History:
The web-app had a bit more than 100'000 hits during December 2015, mainly from the US. It was run on Google Cloud Engine.
Number of unique users was about 17'000. Maximum hit per IP was about 500. Loadbalancing technology was not used.
The containers were automatically restarted each hour ( external script, not included in github).
In December 2015, we ran a US-server and a "rest-of-the-world" server.
( remark: the .pdf - download format was not A4 in the US )
Main traffic was during 26th-28th December 2015.

# Build and run the container

clone the repository with git:

git clone https://github.com/potf0815/myhohoho

cd myhohoho

docker build -t myhohoho_apache_00001 .

To run the container with apache starting in daemon-mode:

docker run -p 80:80 -d myhohoho_apache_00001 apachectl -D FOREGROUND

Now, you will be able to access the app at

http://youripadress/

# History
- Nov/Dec 2015:
created, build and used on Google Cloud Engine

- 22nd Jan 2017:
released on github

 
