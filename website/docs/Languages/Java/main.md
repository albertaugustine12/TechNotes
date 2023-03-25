---
id: java setup
description: notes about java setup and related issues
slug: kafka-setup
sidebar_position: 1
tags:
  - Java
  - jvm
  - jdk
---

# Java

## Setting up multiple version locally

### Using Homebrew
[Stack Overflow Ref](https://stackoverflow.com/questions/26252591/mac-os-x-and-multiple-java-versions)
* homebrew-cask to install the versions of java
* jenv to manage the installed versions of java

Steps to install
```bash
brew install jenv

brew tap homebrew/cask-versions

brew search java

// brew install --cask java11

brew install java11

jenv add <JAVA_PATH>

```

Steps to set a version
```bash
jenv versions

jenv local 11.0.2
```


**Java Paths in mac**

* Built-in JRE default: /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin/Contents/Home
* JDKs downloaded from Apple: /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home/
* JDKs downloaded from Oracle: /Library/Java/JavaVirtualMachines/jdk1.8.0_11.jdk/Contents/Home


### Using sdkman

Refer https://sdkman.io/
