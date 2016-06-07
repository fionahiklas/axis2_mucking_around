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

Using maven to generate the basic layout, this needs a skeleton pom.xml file:

```
<project xmlns="http://maven.apache.org/POM/4.0.0" 
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
	http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.hiklas.mucking.around</groupId>
  <artifactId>BasicAxis2Webapp</artifactId>
  <packaging>war</packaging>
  <version>0.0.1</version>
  <name>Basic Axis2 Web application</name>
  <url>https://github.com/fionahiklas/axis2_mucking_around/</url>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.12</version>
      <scope>test</scope>
    </dependency>
   
    <dependency>
      <groupId>org.mockito</groupId>
      <artifactId>mockito-core</artifactId>
      <version>2.0.54-beta</version>
      <scope>test</scope>
    </dependency>  
  </dependencies>

  <build>
    <finalName>BasicAxis2Webapp</finalName>
  </build>

</project>

```

Then run the following command

```
mvn archetype:generate -DgroupId=com.hiklas.mucking.around -DartifactId=BasicAxis2WebApp =DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
```



## References

### Axis installation

This can be downloaded from the [Apache Axis2 site](http://www.apache.org/dyn/closer.lua/axis/axis2/java/core/1.7.2/axis2-1.7.2-bin.zip)

### Generating Webapp with Maven

Command from this [page](http://www.mkyong.com/maven/how-to-create-a-web-application-project-with-maven/)
