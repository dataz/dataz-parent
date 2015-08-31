dataSet Installer
===============

Installs all DataSet/DataStore Projects. The only purpose is to install all dataSet projects. After you have done it, you can remove this project from your
computer.


Three Simple Steps
==================

1. Clone this repository (or download is as ZIP) from Github.
2. Start installing the actually dataSet projects.
3. Use the installed projects.


How to clone this Repository?
=============================

Just call

    git clone https://github.com/loddar/dataset-install.git


How to Install?
===============

After cloning this repository, you should execute

      ./gradlew install

or under Windows

      gradlew.bat install

This will create (clone) all dataSet projects into a directory (default is ../dataset-projects). If you like to change the target directory, you can use
the *-PtargetDir* Gradle property. If you don't like to call it all the time, change the property in _gradle.properties_.

Example:

    ./gradlew -PtargetDir=$HOME/my/target/directory install

That's it. After installation you found all dataSet projects

    cd ../dataset-projects (or cd $HOME/my/target/directory)
    ./gradlew install


If you like to create IntelliJ IDEA project files, call this:

    ./gradlew idea

or setup Eclipse project files:

    ./gradlew eclipse


How to update?
==============

Just call

    ./gradlew update

or

    ./gradlew -PtargetDir=$HOME/my/target/directory update


Switching to an existing branch
================================

Sometimes it is necessary to switch to a branch. First you muast know which are the existing branches. 

You can resolve them by calling

    ./gradlew show-branches  

or of course 

    ./gradlew -PtargetDir=$HOME/my/target/directory show-branches
     

You will get something like this:

```
    :show-branches
    Show branches of project 'dataset':
    * master
      remotes/origin/HEAD -> origin/master
      remotes/origin/Release0.5
      remotes/origin/master
    Show branches of project 'datastore-sql':
    * master
      remotes/origin/HEAD -> origin/master
      remotes/origin/Release0.5
      remotes/origin/master
    Show branches of project 'datastore-neo4j':
    * master
      remotes/origin/HEAD -> origin/master
      remotes/origin/Release0.5
      remotes/origin/master
```

Now you can switch to an __existing__(!) branch like _Release0.5_ by calling
    
    ./gradlew switch-branch -Dbranch=Release0.5

or 

    ./gradlew -PtargetDir=$HOME/my/target/directory switch-branch -Dbranch=Release0.5
    

The Dependencies
================

Java8 and Git must be installed. You can download it from here:

* [Java 8 SDK on Oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Git](http://git-scm.com/downloads)

Gradle is optional, because you can use the Gradle Wrapper (gradlew). But if you like to download, you can find it [here](https://www.gradle.org/downloads).

Issues
======

If you want to report any issue or feature request (specific to the dataSet Installer), please do it [here](https://github.com/loddar/dataset-install/issues).


Social
======

You can found me on

[Twitter](https://twitter.com/failearly)
[LinkedIn](https://www.linkedin.com/in/markoumek)


License
=======

![GPL v3](http://www.gnu.org/graphics/gplv3-127x51.png)
