#mvnExec

A script to find java files inside your maven project containing a main function without touching `pom.xml`

##Installation

Download and symlink to your path

```bash
$ git clone git@github.com:albfan/mvnExec.git
$ cd mvnExec
$ ln -s $PWD/mvnExec ~/bin/
```

##Usage

mvnExec honors **JDK_HOME**, **JAVA_HOME** system vars and java executable existing in **PATH** (in that order).

launch it from a maven project

```bash
$ cd <maven-project>
$ mvnExec
```

1. First you will see a list of classes having main methods
2. Next you will be prompted for parameters (press `<Enter>` if none is required or launch with `-P`)
3. Program is compiled and launched (launch with `-B` to avoid compiling again)

##Features

Try using `mvnExec --help`

- avoid to change `pom.xml` to test classes with main methods
- **-q** or **--quiet** behave quiet. Don't show noisy [INFO] messages from maven
- Support project classpath resolving for any java version

