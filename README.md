#Intro
Pulling from this repo, **as a new git remote within your existing git project(s)** (see below), will give you [Gradle][2] [wrapper] build goodness, usually where a local [Gradle][2] install isn't available*.

#Getting started adding Gradle wrapper support to your project
Pull the Gradle wrapper into your git project with the following command line (will *not* overwrite your README.md, OK.)

    git init -q; git config core.sparseCheckout true; git remote add gradlewrapper https://github.com/sixman9/gradleWrapperStandalone.git; echo $'*\n!README.md' > .git/info/sparse-checkout; git pull gradlewrapper master  

Then, if you'd like to convert a Maven 'pom.xml' file (to a new 'build.gradle'), for instance, issue:  

    gradlew init  

If you project is empty-ish and you want something useful, try:  

    gradlew init --type "java-library"
                OR
    gradlew init --type "scala-library"

The above assumes you have a [Java JVM][1], [Git][3] and/or a [Git Client][4] installed (of course).  

Gradle Wrapper version = **2.0**  

*This is a small attempt to beat Gradle's 'chicken or the egg' paradox, i.e. no Gradle=>no Gradle Wrapper.  

[1]: https://www.java.com
[2]: http://www.gradle.org
[3]: http://git-scm.com
[4]: http://www.sourcetreeapp.com
