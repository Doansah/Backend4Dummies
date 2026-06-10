## What is Docker

Docker is used to easily run code on multiple different devices. The primary challenge is that there are many different Operating Systems, and versions of every dependency and code. Docker makes it really easy to run written on one device, elsewhere. 

### Images and Containers 

Docker Images, is the description of all the dependencies used by code. Images are written in a *Dockerfile*


Micellaneous things to note: 
-- Layer Caching: Useful to ensure that dependencies are not continuously downloaded, dramatically speeds up build time.
-- .dockerignore file. 

To build an image: 

docker build -t "example" . 

 **Docker Compose**

Docker Compose allows you to manage multiple containers. Lets say your building a web application, with frontend, backend, and DB. You could use one huge container for all of that (you shouldn't), so instead you would use multiple containers, and this is where docker compose becomes really useful. 

Docker Volume is simply a file on our machine that allows our containers to share data / state overtime. 

-- also you can just use docker init (LOL)


### Containers vs Virtualization 


Both of these approaches **ABSTRACT software from underyling hardware** 

**Virtualization** emulates entire physical computers to run multiple operating systems.

How do VM's work? (The hypervisor)

A hypervisor, or a virtual machine monitor acts as the higherst software layer, allowing multiple operating systesm to run alongside eachother orchestrating resources as needed. 

How do Containers work? 

Containers package application code, libraires and config files into an **image**. The run as isolated proceess ontop of the host operating system. 


**Containerization** isolates individual applications and their dependences allowing them to share a single OS kernel. 




