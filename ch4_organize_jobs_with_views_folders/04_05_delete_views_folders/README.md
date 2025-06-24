# 04_05 Delete views and folders

In this lesson, you'll learn the important differences between deleting a view and deleting a folder in Jenkins.

> [!IMPORTANT]
> Deleting folders is permanent and impacts everything inside them, so it’s critical to understand the consequences.

- **Deleting a View:**
  - Views are organizational tools for displaying jobs based on filters or criteria.
  - Deleting a view:
    - Removes the view itself.
    - **Does NOT delete** any jobs, folders, or other items shown in the view.
  - Example: After deleting the **BUILD** view, the jobs with `build` in the name remain accessible in their folders.

- **Deleting a Folder:**
  - Folders act as containers for jobs, views, and other folders.
  - Deleting a folder:
    - Removes the folder permanently.
    - **Deletes everything inside the folder**, including:
      - Jobs
      - Views
      - Other subfolders
  - There is no undo option; the contents are permanently removed.

> [!CAUTION]
> **Be cautious when deleting folders**. Review the folder contents to ensure you aren't unintentionally deleting jobs or configurations you still need.

<!-- FooterStart -->
---
[← 04_04 Search with the command palette](../04_04_search_with_the_command_palette/README.md) | [04_06 Challenge Create Folders and Views →](../04_06_challenge_create_folders_views/README.md)
<!-- FooterEnd -->
