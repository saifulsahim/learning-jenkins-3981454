# 04_03 Create a folder

In this lesson, you'll learn how to use folders in Jenkins to organize jobs and other items. Folders provide a simple, scalable way to group related jobs, making large Jenkins environments much easier to manage.

- **Why Use Folders:**
  - Helps organize jobs by team, project, or purpose.
  - Folders create separate namespaces, allowing jobs in different folders to share the same name without conflict.
  - Folders can also contain views and even other folders.

- **Creating a Folder:**
  - From the Jenkins Dashboard, select **New Item**.
  - Enter a name for the folder (e.g., `Cyclones`).
  - Select **Folder** as the item type and click **OK**.
  - Add a description for the folder (optional, but recommended).
  - Save the folder.

- **Moving Jobs Into a Folder:**
  - Use the pull-down menu next to each job and select **Move**.
  - Choose the desired folder and click **Move**.
  - Repeat for each job—jobs can only be moved one at a time through the interface.

- **Views and Folders:**
  - After moving jobs into folders, views created at the top level won’t show those jobs by default.
  - Edit the view and enable **Recurse in subfolders** to include jobs located inside folders.
  - This allows you to maintain organized folders and still use views to filter jobs across the entire structure.

- **Summary:**
  - Folders and views work together to keep your Jenkins environment clean, organized, and easy to navigate.

<!-- FooterStart -->
---
[← 04_02 Create a view](../04_02_create_a_view/README.md) | [04_04 Search with the command palette →](../04_04_search_with_the_command_palette/README.md)
<!-- FooterEnd -->
