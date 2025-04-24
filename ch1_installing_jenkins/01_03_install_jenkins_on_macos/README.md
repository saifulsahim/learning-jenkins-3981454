# 01_03 Install Jenkins on macOS

Use these instructions to install Jenkins on a system running a macOS operating system.

## **Prerequisites**

Before installing Jenkins, make sure that the system has the following in place:

* A recent version of the macOS operating system (for example, macOS 15 Sequoia)
* At least **256 MB of RAM**
* At least **1 GB of drive space**

You should have **administrator privileges** to complete the installation.

## **Install the Homebrew package manager**

You will use the Homebrew package manager to install Jenkins and its dependencies.

Use the instructions from the link below to install Homebrew:

* [https://brew.sh/](https://brew.sh/)

## **Install Java 21 JDK**

Systems operating Jenkins must have a Java runtime environment installed.

The recommended version of Java for use with Jenkins is Java 21\.  The Java Development Kit (JDK) version includes the Java runtime environment and additional development tools.

1. Open a terminal on the macOS system.
1. Install openjdk@21:
   1. `brew install openjdk@21`
1. Confirm that the installation completes successfully.

## **Install Jenkins**

1. In the terminal, run the following command:
   1. `brew install jenkins`
1. Confirm that the installation completes successfully.
1. Run Jenkins as a service with the following command:
   1. `brew services start jenkins`
1. Retrieve the initial administrator password:
   1. `cat ~/.jenkins/secrets/initialAdminPassword`
1. Copy the password for use during the next installation steps
1. Complete the installation by opening the following URL in a browser:
   1. [`http://localhost:8080`](http://localhost:8080)

<!-- FooterStart -->
---
[← 01_02 Install Jenkins on Windows](../01_02_install_jenkins_on_windows/README.md) | [01_04 Install Jenkins on Ubuntu →](../01_04_install_jenkins_on_ubuntu/README.md)
<!-- FooterEnd -->
