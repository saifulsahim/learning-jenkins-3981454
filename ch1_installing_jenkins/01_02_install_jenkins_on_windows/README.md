# 01_02 Install Jenkins on Windows

Use these instructions to install Jenkins on a system running a Windows operating system.

## **Prerequisites**

Before installing Jenkins, make sure that the system has the following in place:

* A recent version of the Windows operating system (for example, Windows 11, Windows Server 2022-2025)
* At least **256 MB of RAM**
* At least **1 GB of drive space**

You should have **administrator privileges** to complete the installation.

## **Install Java 21 JDK**

Systems operating Jenkins must have a Java runtime environment installed.

The recommended version of Java for use with Jenkins is Java 21.  The Java Development Kit (JDK) version includes the Java runtime environment and additional development tools.

1. Download the [Microsoft Build of OpenJDK](https://learn.microsoft.com/en-us/java/openjdk/download#openjdk-21) for Windows x64:  [https://aka.ms/download-jdk/microsoft-jdk-21.0.6-windows-x64.msi](https://aka.ms/download-jdk/microsoft-jdk-21.0.6-windows-x64.msi)

    ![Download the Microsoft Build of OpenJDK for Windows x64](images/01_02_install_jenkins_on_windows-java-1.png)

1. Open the installation package. Select **Next**.

    ![Open the installation package. Select Next.](images/01_02_install_jenkins_on_windows-java-2.png)

1. Accept the license agreement and select **Next**.

    ![Accept the license agreement and select Next.](images/01_02_install_jenkins_on_windows-java-3.png)

1. Select "**Install for all users of this machine**" and select **Next**.

    ![Select "Install for all users of this machine" and select Next.](images/01_02_install_jenkins_on_windows-java-4.png)

1. Select "**Set or override JAVA\_HOME variable**" and select **Next**.

    ![Select "Set or override JAVA\_HOME variable" and select Next.](images/01_02_install_jenkins_on_windows-java-5.png)

1. Select **Install**.

    ![Select Install and wait for the installation to complete.](images/01_02_install_jenkins_on_windows-java-6.png)

1. When the installation completes, select **Finish**.

    ![When the installation completes, select Finish.](images/01_02_install_jenkins_on_windows-java-7.png)

### **Install Git**

A `git` installation is required for Jenkins to connect to code repositories.

1. Download the latest version of the Git installer from the following link: [https://git-scm.com/downloads/win](https://git-scm.com/downloads/win)

    ![Download the latest version of the Git installer for Windows.](images/01_02_install_jenkins_on_windows-git-1.png)

1. Open the installation package.
1. Accept all defaults and select **Next** on each screen of the installation dialog.

    ![Start the installation and accept "Next" on each screen.](images/01_02_install_jenkins_on_windows-git-3.png)

1. On the "Configuring extra options" screen, select **Install**.
1. When the installation completes, select **Finish**.

    ![Complete the installation.](images/01_02_install_jenkins_on_windows-git-5.png)

## **Install Jenkins**

1. Download the LTS version of Jenkins for Windows from the Jenkins download webpage: [https://www.jenkins.io/download/](https://www.jenkins.io/download/)

    ![Download the LTS version of Jenkins for Windows.](images/01_02_install_jenkins_on_windows-jenkins-01.png)

1. Open the installation package.  Select **Next**.

    ![Open the installation package.  Select Next.](images/01_02_install_jenkins_on_windows-jenkins-02.png)

1. On the "Destination Folder" screen, select **Next**.

    ![On the "Destination Folder" screen, select Next.](images/01_02_install_jenkins_on_windows-jenkins-03.png)

1. On the "Service Logon Credentials" screen, select "Run service as LocalSystem (not recommended)". Select **Next**. *NOTE: This option is acceptable for learning purposes in a controlled environment*.

    ![On the "Service Logon Credentials" screen, select "Run service as LocalSystem (not recommended)". Select Next.](images/01_02_install_jenkins_on_windows-jenkins-04.png)

1. On  the "Port Selection" screen, select **Test Port**.  Select **Next**.  *NOTE: If the port test fails, check for other processes that are running on the system and using port `8080`.  Stop the other process or consider using a different port for Jenkins*.

    ![On  the "Port Selection" screen, select Test Port.](images/01_02_install_jenkins_on_windows-jenkins-05-1.png)

    ![After testing the port, select Next.](images/01_02_install_jenkins_on_windows-jenkins-05-2.png)

1. On the "Select Java home directory" screen, select **Change...**.

    ![On the "Select Java home directory" screen, select Change...](images/01_02_install_jenkins_on_windows-jenkins-06.png)

1. Inside the "Program Files" directory, select "Microsoft"; then select "jdk-21.0.6.7-hotspot".

    ![Inside the "Program Files" directory, select "Microsoft"; then select "jdk-21.0.6.7-hotspot".](images/01_02_install_jenkins_on_windows-jenkins-07.png)

1. Select **OK** then select **Next**.

    ![Select OK then select Next.](images/01_02_install_jenkins_on_windows-jenkins-08.png)

1. On the "Custom Setup" screen, select **Next**.

    ![On the "Custom Setup" screen, select Next.](images/01_02_install_jenkins_on_windows-jenkins-09.png)

1. Select **Install**.

    ![Select Install.](images/01_02_install_jenkins_on_windows-jenkins-10.png)

1. When the installation completes, select **Finish**.

    ![When the installation completes, select Finish.](images/01_02_install_jenkins_on_windows-jenkins-11.png)

1. Open a File Explorer window and browse to the following path: `C:\ProgramData\Jenkins\.jenkins\secrets\initialAdminPassword`

    ![Open a File Explorer window and browse to the following path: C:\\ProgramData\\Jenkins\\.jenkins\\secrets\\initialAdminPassword](images/01_02_install_jenkins_on_windows-jenkins-12.png)

1. Select **Notepad** as the application to open the file.  Then select **Just once**.

    ![Select Notepad as the application to open the file.  Then select Just once.](images/01_02_install_jenkins_on_windows-jenkins-13.png)

1. Inside Notepad, copy the initial admin password.

    ![Inside Notepad, copy the initial admin password.](images/01_02_install_jenkins_on_windows-jenkins-14.png)

1. Complete the installation by opening a browser and connecting to localhost:8080: [http://localhost:8080](http://localhost:8080)

<!-- FooterStart -->
---
[← 01_01 System requirements](../01_01_system_requirements/README.md) | [01_03 Install Jenkins on macOS →](../01_03_install_jenkins_on_macos/README.md)
<!-- FooterEnd -->
