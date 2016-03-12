# groovemachine
Dockerfile for a huge centos image with dev libraries for audio work, python2 and python3

This image was specifically made to install [Libgroove](https://github.com/andrewrk/libgroove) and run audio workers under python. It specifically installs the version 4.3.0 of libgroove and compiles many libraries required by libgroove from source. 
Based on Centos:7
Includes: Nodejs, NPM, python2 and python3 along with supervisor.  Flask is installed within python3.

There is no entrypoint or cmd in this image. It is intended to be used within your own dockerfiles where you may run some applications that requires libgroove.

Supervisord allows one to place configuration files in /etc/supervisor.d/

Mount your application folder in /opt/apps/ 

Python3 is placed within the path as "python".  

On Docker Hub:
https://hub.docker.com/r/amalhotra/groovemachine/
