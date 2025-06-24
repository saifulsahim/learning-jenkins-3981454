# 01_09 Manage Tools

Jenkins allows you to centrally manage tools like Maven, Java, and Git so they can be used across all your jobs. In this lesson, you’ll learn how to configure these tools through the Jenkins interface.

- **Accessing Tool Configuration:**
  - From the Jenkins Dashboard, select **Manage Jenkins → Tools**.

- **Configuring Tools (Example: Maven):**
  - Under **Maven Installations**, select **Add Maven**.
  - Provide a descriptive name, typically including the version number (e.g., `Maven-3.9.9`).
  - You can install multiple versions if needed.
  - Check the box for **automatic installation** to have Jenkins install the tool the first time it's required.
  - Always **Save** or **Apply** your changes before leaving the page.

- **Windows Users:**
  - Be sure to configure **Git** separately if you're following along on a Windows system.
  - Review the exercise files for  installation instructions and more information:
    - [01_02 Install Jenkins on Windows](../01_02_install_jenkins_on_windows/README.md)

<!-- FooterStart -->
---
[← 01_08 Manage Plugins](../01_08_manage_plugins/README.md) | [01_10 Challenge: Set Up a Jenkins Server on Windows →](../01_10_challenge_set_up_a_jenkins_server_on_windows/README.md)
<!-- FooterEnd -->
