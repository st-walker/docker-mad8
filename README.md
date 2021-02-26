# docker-mad8
Docker image for running the DESY version of MAD8.  My motivation was that I wanted to run MAD8 on MacOS to make my life easier.

I do not bundle the sources here and I have not uploaded this to Docker hub because I don't know anything about the licensing of the source or any binaries found on the web.  You must build it yourself but it is easy to do so.

## Building the MAD8 image

1. Clone this repo
3. `$ docker build --tag mad8 docker-mad8/mad8`
4. `$ docker run -i mad8 < myfile.mad8 `

## Alternative solutions that I am aware of

and why I don't use them:

- http://hywelowen.org/running-mad8-on-osx-10-8-mountain-lion/ - Uses 32bit binaries so this doesn't work on later MacOS versions that have abandoned support for 32bit executables.
- https://hub.docker.com/r/manacc/mad8/ - Doesn't work.  Original Dockerfile and sources nowhere to be found so I couldn't try to fix, which motivated me to make this.
- https://github.com/manacc/mad8 - I couldn't get it to compile; I got some strange linker errors and I gave up rather quickly.
