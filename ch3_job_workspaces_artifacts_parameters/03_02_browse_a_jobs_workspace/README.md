# 03_02 Browse a job's workspace

In this lesson, you'll learn how to explore a job's workspace in Jenkins. The workspace is where files are stored during a build, and understanding how to access and clean up this area is essential for managing jobs effectively.

- **Understanding the Workspace:**
  - Each Jenkins job has its own dedicated directory called the **workspace**.
  - The workspace stores files generated or checked out during the build process.

- **Browsing the Workspace:**
  - From the job's page, select the **Workspace** link.
  - You can:
    - View files and directories from source code or build output.
    - Open directories to see additional files.
    - Select files to download or view their contents (browser behavior may vary).

- **Cleaning the Workspace:**
  - Select **Wipe out current workspace** to manually delete all files from the workspace.
  - After wiping the workspace, running a new build will recreate the workspace and necessary files.

- **Automating Workspace Cleanup:**
  - In the **Environment** section of job configuration, enable **Delete workspace before build starts** to clean the workspace before each run.
  - You can also add a **Post-Build Action** to automatically delete the workspace after a build finishes.

> [!TIP]
> If your project generates files you want to keep, you’ll need to configure them as **artifacts**, covered in the next lesson.

<!-- FooterStart -->
---
[← 03_01 Using a global build tool](../03_01_using_a_global_build_tool/README.md) | [03_03 Manage artifacts →](../03_03_manage_artifacts/README.md)
<!-- FooterEnd -->
