# Overview

This image is used to build the book "Modelica by Example" which is located at:

https://github.com/xogeny/ModelicaBook

The `Dockerfile` here creates an Ubuntu 16.04 based image that installs
OpenModelica (1.12.0), Python, Sphinx and a variety of other tools
required in order to build the book.

This image can then be used either to build the book locally on any
machine that can host Docker containers or via a CI system like
CircleCI.

Note that the book source should be mounted as a volume when running the
Docker container, e.g.,

```
docker run -v <MBE_Source>:/opt/MBE/ModelicaBook -i -t mtiller/book-builder make book
```

