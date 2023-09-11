# Docker-Projects
Running php with Apache on Docker

STEP # 1
First we create 2 files,
one is php file, and the othe is a Dockerfile.

a) Docker php with Apache

vim index.php

<?php
echo "Welcome to Alnafi</br>"; echo
"Running php with Apache on Docker";
?>

b) vim Dockerfile

vim Dockerfile

FROM php:7.4-apache
COPY . /var/www/html

STEP # 2

To Build Docker Image, command is
docker build -t img-php-apache-example .


To Run the Docker Image
docker run -it -d -p 8080:80 img-php-apache-example
