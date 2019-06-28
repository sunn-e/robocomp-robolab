<img align="left" width="120" height="120" src="https://avatars2.githubusercontent.com/u/6409012?s=200&v=4">

# Hakuyo-RoboComp Component

[![Open Issues](https://img.shields.io/github/issues-raw/robocomp/robocomp-robolab.svg?color=%23ff7b25&style=for-the-badge)]( https://github.com/robocomp/robocomp-robolab/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/robocomp/robocomp-robolab.svg?color=8a00d4&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/pulls)
[![Contributors](https://img.shields.io/github/contributors/robocomp/robocomp-robolab.svg?color=%233b3a30&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/graphs/contributors)
[![Code size](https://img.shields.io/github/languages/code-size/robocomp/robocomp-robolab.svg?color=12e6c8&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab)
[![Join the chat at https://gitter.im/robocomp/robocomp](https://img.shields.io/gitter/room/robocomp/robocomp-robolab.svg?color=6b48ff&style=for-the-badge)](https://gitter.im/robocomp/robocomp?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![LICENSE](https://img.shields.io/github/license/robocomp/robocomp-robolab.svg?color=2f89fc&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/blob/master/LICENSE)
![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/robocomp/robocomp-robolab.svg?style=for-the-badge)
[![Website](https://img.shields.io/website/https/github.io.svg?color=8a00d4&style=for-the-badge)](https://robocomp.github.io/web/)


## Introduction
### RoboComp
RoboComp is an open-source Robotics framework providing the tools to create and modify software components that communicate through public interfaces. Components may *require*, *subscribe*, *implement* or *publish*
interfaces in a seamless way. Building new components is done using two domain specific languages, IDSL and CDSL. With IDSL you define an interface and with CDSL you specify how the component will communicate with the world. With this information, a code generator creates C++ and/or Python sources, based on CMake, that compile and execute flawlessly. When some of these features have to be changed, the component can be easily regenerated and all the user specific code is preserved thanks to a simple inheritance mechanism.
### Hokuyo
What are Hokuyos?

A Hokuyo is a piece of software that adheres to a small set of guidelines standardizing some aspects of how other things interact with the Hokuyo. The primary purpose is to make it easier to integrate many smaller pieces of software together into a larger system by agreeing on how Hokuyos present their external interfaces. More concretely, the guidelines dictate where a Hokuyo places its public-facing files -- executables, header files, libraries, python modules, jar files, etc.

A Hokuyo can be as simple or as complex as necessary, providing anything from a single shell script to a set of libraries and tools written in multiple programming languages. It's important to note that the Hokuyos policies enforce no restrictions on the internal structure and organization of a Hokuyo, and are primarily concerned with the external aspects -- the parts of the software that other people or programs interact with.
Why Hokuyos?

When developing a new piece of software, one issue is how to organize the software's external aspects. For example, if building a few executables, where do those executables get placed? If building a library of useful functions for other programs to use, where should the public header files and the compiled library files go?

On most operating systems, there are well-known standards if the software is to be installed system-wide (e.g., header files go in /usr/include). However, a lot of software is not meant to be installed to a system-wide location, and the organization of this kind of software is usually decided by the individual programmer, with the end result being lots of people making lots of different choices.

This becomes a problem when people want to share software, as it introduces the extra headache of integrating build systems, messing with Makefiles, juggling files and directories around, etc. Organizational practices that worked for one person and one piece of software may no longer work for larger systems, and the seemingly simple task of two people trying to collaborate quickly becomes a build system nightmare.

The primary motivation behind Hokuyos is to introduce some policies governing software that might be shared with others, but may not be intended for system-wide installation. The driving design principles are simplicity and modularity, to make it easier for researchers to develop software that others can use.


### Configuration parameters
As any other component,
``` *hokuyo* ```
needs a configuration file to start. In

    etc/config

you can find an example of a configuration file. We can find there the following lines:

    EXAMPLE HERE

    
### Starting the component
To avoid changing the *config* file in the repository, we can copy it to the component's home directory, so changes will remain untouched by future git pulls:

    cd

``` <hokuyo 's path> ```

    cp etc/config config
    
After editing the new config file we can run the component:

    bin/

```hokuyo ```

    --Ice.Config=config
    
---
You can find more tutorials on RoboComp in [tutorials](doc/README.md) 

Drop comments and ask questions in:

- https://groups.google.com/forum/?hl=en#!forum/robocomp-dev
- https://gitter.im/robocomp

Please, report any bugs to pbustos@unex.es

If you have any suggestions to improve the repository, like features or tutorials, please contact: robocomp.team@gmail.com 

---

Copyright (C) 2019 by [Sunny Dhoke](https://github.com/sunn-e) for [Robocomp project.](https://github.com/robocomp) as a GSoD assignment.
