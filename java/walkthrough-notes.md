This walkthrough was a demonstration of deploying a java17 application onto an EC2 Instance.

A jar file was created from the project source code and delivered to the EC2 instance via git
  - a jar file contains all of the dependencies needed to run the application

## EC2 Instance Configuration

A jar file is not enough to start and run a java application on a fresh server. A JRE or JDK is still necessary. Knowing that the project was using java17 installing the appropriate jre is an easy task.

This walkthrough installed openjdk-17-jre:

```bash
openjdk-17-jre/jammy-security,jammy-updates,now 17.0.8.1+1~us1-0ubuntu1~22.04 amd64 [installed,automatic]
  OpenJDK Java runtime, using Hotspot JIT
```


