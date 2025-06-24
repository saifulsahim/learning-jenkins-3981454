# 02_01 Your first jenkins job

In this lesson, you’ll create your first Jenkins job—a simple "Hello World" project. This helps confirm your Jenkins setup is working and introduces you to basic job configuration.

- **Creating a New Job:**
  - From the Jenkins Dashboard, select **New Item**.
  - Enter a name like `Hello-World` (avoid spaces to prevent issues with command-line or API interactions).
  - Select **Freestyle Project** and click **OK**.

- **Configuring the Job:**
  - On the configuration page, scroll to the **Build** section.
  - Select **Add build step**:
    - For Windows: **Execute Windows batch command**
    - For Mac, Linux, or Docker: **Execute shell**
  - Enter the following command:

    ```bash
    echo "Hello, world"
    ```

  - Click **Apply** to save progress, then **Save** to finalize the job configuration.

- **Running the Job:**
  - Click **Build Now** on the job homepage.
  - Once the build completes, check the **Build History** for a green checkmark and build number.
  - Click the checkmark to view the console output, where you’ll see your "Hello, world" message and a success status.

<!-- FooterStart -->
---
[← 01_11 solution Set Up a Jenkins Server on Windows](../../ch1_installing_jenkins/01_11_solution_set_up_a_jenkins_server_on_windows/README.md) | [02_02 Job types →](../02_02_job_types/README.md)
<!-- FooterEnd -->
