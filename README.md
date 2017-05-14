# X11

A docker image for minimal X11 running enviroment, inspired by suchja/x11client and suchja/x11server.

The original suchja X11 design have two seperate parts, server and client. It is fine but for many purpose, but I think I can combine them together for simplicity use.

## Purpose

Is is a base for another image mythay/wine to run windows software on Linux.
 

## Usage

You can start a X11 container like this:

`docker run --rm -it -e VNC_PASSWORD=newPW -p 5900:5900 mythay/x11 /bin/bash`

Then you enter the container's shell, then you can run 

`rxvt`

You can see the window if you use a VNC Viewer connect to the container.

**ATTENTION:** It's important that the `startx11.sh` script is executed. So if you like to supply your own `ENTRYPOINT` in an image derived from this, ensure that the `/startx11.sh` is executed first thing during container startup.


