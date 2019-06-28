<img align="left" width="120" height="120" src="https://avatars2.githubusercontent.com/u/6409012?s=200&v=4">

# Hokuyo-RoboComp Component

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

Hello there 😄, RoboComp is an open-source 💜  Robotics framework. It provides tools to create and modify software components that communicate through public interfaces. Components may *require*, *subscribe*, *implement* or *publish*
interfaces in a seamless way. Building new components is done using two domain specific languages, IDSL and CDSL. With IDSL you define an interface and with CDSL you specify how the component will communicate with the world 🌏. With this information, a code generator creates C++ and/or Python sources, based on CMake, that compile and execute flawlessly. When some of these features have to be changed, the component can be easily regenerated and all the user specific code is preserved thanks to a simple inheritance mechanism.

### HokuyoComp 🤖

![hokuyo logo](https://github.com/sunn-e/Open-source-assets/blob/master/hokuyo.svg)

#### What is HokuyoComp🤖?

HokuyoComp is a component used by Robocomp.

#### What does it do?

HokuyoComp helps to utilise laser sensor.

#### What languge is it build in?

HokuyoComp is written in C++11

### Configuration parameters
First, You may install robocomp by following the instructions mentioned [here](https://github.com/robocomp/robocomp/blob/stable/README.md).

As any other component,

``` hokuyo ```

needs a configuration file to start. In
```
    etc/config
```
you can find an example of a configuration file. We can find there the following lines:
```
    Will soon add a working example here. Till then you may want to create an issue or ping us on Gitter.
```
### Starting the component

-   To avoid changing the *config* file in the repository, we can copy it to the component's home directory, so changes will remain untouched by future git pulls:
```
cd <hokuyo 's path>

cp etc/config config
```   

-   After editing the new config file we can run the component:

```
bin/hokuyo

--Ice.Config=config
    
```

---
You can find more tutorials on RoboComp in [tutorials](doc/README.md) 

## Contributing 💻

### Follow the Coding Style 

#### Well formed example

```cpp
class MyClass
{
public:
  MyClass(int t_data)
    : m_data(t_data)
  {
  }
  
  int getData() const
  {
    return m_data;
  }
  
private:
  int m_data;
};
```
#### Distinguish C++ Files From C Files

#### Comments

Comment blocks should use `//`, not `/* */`. Using `//` makes it much easier to comment out a block of code while debugging.

```cpp
// this function does something
int myFunc()
{
}
```
#### Keep lines a reasonable length

```cpp
// Bad Idea
// hard to follow
if (x && y && myFunctionThatReturnsBool() && caseNumber3 && (15 > 12 || 2 < 3)) { 
}

// Good Idea
// Logical grouping, easier to read
if (x && y && myFunctionThatReturnsBool() 
    && caseNumber3 
    && (15 > 12 || 2 < 3)) { 
}
```
#### Use "" For Including Local Files
... `<>` is [reserved for system includes](http://blog2.emptycrate.com/content/when-use-include-verses-include).

```cpp
// Bad Idea. Requires extra -I directives to the compiler
// and goes against standards
#include <string>
#include <includes/MyHeader.hpp>

// Worse Idea
// requires potentially even more specific -I directives and 
// makes code more difficult to package and distribute
#include <string>
#include <MyHeader.hpp>
```
#### Forward Declare when Possible

This:
```cpp
// some header file
class MyClass;

void doSomething(const MyClass &);
```

instead of:

```cpp
// some header file
#include "MyClass.hpp"

void doSomething(const MyClass &);
```

This is a proactive approach to simplify compilation time and rebuilding dependencies.

#### Always Use Namespaces 

There is almost never a reason to declare an identifier in the global namespaces. Instead, functions and classes should exist in an appropriately named namespaces or in a class inside of a namespace. Identifiers which are placed in the global namespace risk conflicting with identifiers from other (mostly C, which doesn't have namespaces) libraries.

#### Avoid Compiler Macros 

Compiler definitions and macros are replaced by the pre-processor before the compiler is ever run. This can make debugging very difficult because the debugger doesn't know where the source came from.

```cpp
// Good Idea
namespace my_project {
  class Constants {
  public:
    static const double PI = 3.14159;
  }
}

// Bad Idea
#define PI 3.14159;
```
### Sending Pull Requests ✔️

-   Clone the repo from https://github.com/robocomp/robocomp-robolab
-   Make some changes in a new branch
-   Test it yourself.
-   Send Pull Request to Main robocomp-robolab repository.
-   Add appropriate labels.
-   Wait for the input by other contributors.
-   Make changes if suggested. If everything is working fine, your pul request will be merged. :) Congratulations. You just helped RoboComp community. We like you. :p

## Discussion 💬 
Drop comments and ask questions in:

- https://groups.google.com/forum/?hl=en#!forum/robocomp-dev
- https://gitter.im/robocomp

Please, report any bugs to pbustos@unex.es

If you have any suggestions to improve the repository, like features or tutorials, please contact: robocomp.team@gmail.com 

### Notes 📑

The documentation is a work in progress. Stay tuned for more. In case you need any help, please reach out to us on our gitter. {Take me there now](https://gitter.im/robocomp/robocomp) 

---
[![Open Issues](https://img.shields.io/github/issues-raw/robocomp/robocomp-robolab.svg?color=%23ff7b25&style=for-the-badge)]( https://github.com/robocomp/robocomp-robolab/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/robocomp/robocomp-robolab.svg?color=8a00d4&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/pulls)
[![Contributors](https://img.shields.io/github/contributors/robocomp/robocomp-robolab.svg?color=%233b3a30&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/graphs/contributors)
[![Code size](https://img.shields.io/github/languages/code-size/robocomp/robocomp-robolab.svg?color=12e6c8&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab)
[![Join the chat at https://gitter.im/robocomp/robocomp](https://img.shields.io/gitter/room/robocomp/robocomp-robolab.svg?color=6b48ff&style=for-the-badge)](https://gitter.im/robocomp/robocomp)
[![LICENSE](https://img.shields.io/github/license/robocomp/robocomp-robolab.svg?color=2f89fc&style=for-the-badge)](https://github.com/robocomp/robocomp-robolab/blob/master/LICENSE)
![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/robocomp/robocomp-robolab.svg?style=for-the-badge)
[![Website](https://img.shields.io/website/https/github.io.svg?color=8a00d4&style=for-the-badge)](https://robocomp.github.io/web/)

---

Copyright (C) 2019
Made with 💜,💻 and ☕️ by [Sunny Dhoke](https://github.com/sunn-e) for [Robocomp project](https://github.com/robocomp) as a GSoD assignment.
