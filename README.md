## Overview

Example Axis 2 Client and server to understand what generation of axis2 code achieves and how to write clients and servers.

## Help

### JAVA_HOME on MacOS

Both Linux and MacOS have weird-ass layouts for their native JVM installations, for the latter the JAVA_HOME environment variable (that axis2 needs to run) is as follows

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_40.jdk/Contents/Home/
```

## Creating Basic Project

I want to just build things up from basic components and not rely on axis2 to do all of the work.  Ideally this is what I want

* Simple Spring web app
* Web app contains an axis servlet that exposes the services
* Generated code is held in target not in src
* Axis2 isn't used to generate any implementation skeltons
* Everything this TDD!
* Everything is neat and simple :)

### Maven Project Creation

Using maven to generate the basic layout run the following command

```
mvn archetype:generate -DgroupId=com.hiklas.mucking.around -DartifactId=BasicAxis2WebApp -Dversion=0.0.1 -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
```



## References

### Axis installation

This can be downloaded from the [Apache Axis2 site](http://www.apache.org/dyn/closer.lua/axis/axis2/java/core/1.7.2/axis2-1.7.2-bin.zip)

### Generating Webapp with Maven

Command from this [page](http://www.mkyong.com/maven/how-to-create-a-web-application-project-with-maven/)
