# 04_06 Challenge Create Folders and Views

In this challenge you will create folders and views to support growing development teams and their Jenkins projects.

## **Challenge Overview**

The Engineering and Accounting teams are using Jenkins for application development.  Each team has projects that build and deploy applications. You will help them create an organized, scalable layout using folders and views.  After creating folders and views, use the command palette to demonstrate how the teams can find their jobs quickly.

## **Instructions**

1. **Create four, empty jobs with the following names (note that the jobs do not need to include any additional configuration or build steps)**

   - `Accounting-Build`
   - `Accounting-Deploy`
   - `Engineering-Build`
   - `Engineering-Deploy`

2. **Create views based on job type**

   - Create one view named **Build** that shows jobs matching the regular expression `.*Build.*`
   - Create one view named **Deploy** that shows jobs matching the regular expression `.*Deploy.*`
   - Configure the views to recurse into subfolders

3. **Create a new job named `Engineering-build-ui`**

   - Confirm that the job is automatically included in the appropriate view based on your regular expression.

4. **Create folders by team and relocate jobs according to their name**

   - Create a folder named **Engineering**.
   - Create a folder named **Accounting**.
   - Move jobs into the appropriate folder.
   - Confirm that the jobs are still visible in their associated view

5. **Use the command palette for navigation**.

   - Open the `Engineering-Build` job
   - Navigate directly to the **Accounting** folder.

This challenge should take 10 to 15 minutes.

<!-- FooterStart -->
---
[← 04_05 Delete views and folders](../04_05_delete_views_folders/README.md) | [04_07 Solution Create Folders and Views →](../04_07_solution_create_folders_views/README.md)
<!-- FooterEnd -->
