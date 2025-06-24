# 04_02 Create a view

In this lesson, you'll learn how to create views in Jenkins to organize and display groups of jobs based on name patterns or other criteria. Views help keep large Jenkins servers clean and easy to navigate.

## **Preparing for the Demonstration**

Create at least three jobs with names that make it easy to organize them into views:

1. A job with **"build"** in the name, for example: `app-build`
1. A job with **"test"** in the name, for example:  `app-test`
1. A job with **"deploy"** in the name, for example: `app-deploy`

Creating jobs with clear, consistent naming will make it easier to test your views and apply filtering with regular expressions.

## **Demonstration**

- **Creating a New View:**
  - Click the **"+"** sign next to the **All** tab (which itself is a view showing all jobs and folders).
  - Enter a descriptive name for the view (e.g., `build`).
  - Select **List View** and click **Create**.

- **Configuring the View:**
  - Add a description for the view (e.g., "These are the build jobs.").
  - Under the **Jobs** section, you can:
    - Manually select jobs to include, OR
    - Use a **Regular Expression** to automatically include jobs based on name patterns.

- **Example Regular Expression:**
  - To include all jobs with "build" in their name:

    ```java
    .*build.*
    ```

  - This matches all existing and future jobs with `build` anywhere in the name.

- **Final Steps:**
  - Click **Save** to create the view.
  - The new view will appear as a tab next to **All**, showing only the filtered jobs.

> [!TIP]
> Repeat the same steps to create views for `test` and `deploy` jobs using similar naming patterns.

<!-- FooterStart -->
---
[← 04_01 Views and folders](../04_01_views_folders/README.md) | [04_03 Create a folder →](../04_03_create_a_folder/README.md)
<!-- FooterEnd -->
