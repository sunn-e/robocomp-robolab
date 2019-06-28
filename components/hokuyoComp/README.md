<img align="left" width="120" height="120" src="https://avatars2.githubusercontent.com/u/6409012?s=200&v=4">

# Hakuyo

[![Open Issues](https://img.shields.io/github/issues-raw/robocomp/robocomp-robolab.svg?color=%23ff7b25&style=for-the-badge)]( https://github.com/robocomp/robocomp-robolab/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/robocomp/robocomp-robolab.svg?color=8a00d4&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/pulls)
[![Contributors](https://img.shields.io/github/contributors/robocomp/robocomp-robolab.svg?color=%233b3a30&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/graphs/contributors)
[![Code size](https://img.shields.io/github/languages/code-size/robocomp/robocomp-robolab.svg?color=12e6c8&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab)
[![Join the chat at https://gitter.im/robocomp/robocomp](https://img.shields.io/gitter/room/robocomp/robocomp-robolab.svg?color=6b48ff&style=for-the-badge)](https://gitter.im/robocomp/robocomp?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![LICENSE](https://img.shields.io/github/license/robocomp/robocomp-robolab.svg?color=2f89fc&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/blob/master/LICENSE)
![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/robocomp/robocomp-robolab.svg?style=for-the-badge)
[![Website](https://img.shields.io/website/https/github.io.svg?color=8a00d4&style=for-the-badge)](https://robocomp.github.io/web/)

Intro to component here

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


