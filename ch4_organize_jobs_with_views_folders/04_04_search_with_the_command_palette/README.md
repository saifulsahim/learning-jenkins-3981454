# 04_04 Search with the command palette

In this lesson, you'll learn how to quickly search for jobs, folders, builds, and more using the Jenkins command palette. The command palette provides a fast, keyboard-driven way to navigate your Jenkins environment.

The command palette is a fast and efficient tool to navigate large Jenkins environments without clicking through menus.

- **Accessing the Command Palette:**
  - **macOS:** Press `Command + K`.
  - **Windows/Linux:** Press `Control + K`.
  - A search dialog opens where you can enter search terms.

- **What You Can Search For:**
  - Folders
  - Jobs
  - Views
  - Users
  - Specific builds by job name and build number
  - Administrative options like **Manage Jenkins**

- **Example Searches:**
  - Typing `cyclones` displays all folders and jobs with "cyclones" in the name.
  - Typing `build` shows jobs and views related to builds.
  - To jump directly to a specific build, combine search terms:

    ```bash
    cyclones deploy 1
    ```

    - This takes you to build #1 of the `cyclones-deploy` job.

> [!TIP]
> As you get more familiar with Jenkins, experiment with the command palette—additional searchable items may be added in future versions.

<!-- FooterStart -->
---
[← 04_03 Create a folder](../04_03_create_a_folder/README.md) | [04_05 Delete views and folders →](../04_05_delete_views_folders/README.md)
<!-- FooterEnd -->
