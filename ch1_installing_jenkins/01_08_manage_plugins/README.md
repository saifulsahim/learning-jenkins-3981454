# 01_08 Manage Plugins

Plugins are the key to customizing and extending Jenkins to meet your needs. In this lesson, you'll learn how to install, disable, and remove plugins using the Jenkins interface.

### Essential Topics Covered

- **Installing Plugins:**
  - From the Dashboard, select **Manage Jenkins → Plugins**.
  - Under the **Available Plugins** tab, you can:
    - Sort the list by name or release date.
    - Use the search box to quickly filter plugins.
    - Select a plugin name to view full details on the Jenkins website.
    - Check the box next to a plugin and click **Install** to add it to your Jenkins instance.

- **Disabling and Uninstalling Plugins:**
  - On the **Installed Plugins** tab, search for the plugin name.
  - Unchecking the **Enabled** box disables the plugin without removing it.
  - Clicking the red **X** icon begins the uninstall process.
  - Confirm the uninstall when prompted.
  - A message shows the uninstall is pending.
  - Complete the process by adding `/safeRestart` to the Jenkins URL to safely restart Jenkins.

<!-- FooterStart -->
---
[← 01_07 The Jenkins user interface](../01_07_the_jenkins_user_interface/README.md) | [01_09 Manage Tools →](../01_09_manage_tools/README.md)
<!-- FooterEnd -->
