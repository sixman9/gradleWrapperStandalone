#Intro
Pulling from this repo, as a new git remote within your existing git project(s), will give you Gradle [wrapper] build goodness where a Gradle install wasn;t available, locally (i.e. beats the chicken or the egg)

#Getting Started adding Gradle wrapper support to your project
To add the Gradle wrapper to you git-based project, issue the following (can be done on 1-line)

    git remote add gradlewrapper https://github.com/sixman9/gradleWrapperStandalone.git; git pull gradlewrapper master  

Then, if you like to convert a Maven 'pom.xml' file (to a new 'build.gradle'), for instance, issue:  

    gradlew init  

If you project is empty-ish and you want something useful, try:  

    gradlew init --type "java-library"
                OR
    gradlew init --type "scala-library"

The above assumes you have a [Java JVM][1] installed (of course).

[1]: https://www.java.com
