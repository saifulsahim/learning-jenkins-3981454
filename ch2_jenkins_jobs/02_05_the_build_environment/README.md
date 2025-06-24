# 02_05 The build environment

In this lesson, you'll explore the Build Environment, Build Steps, and Post-Build Actions sections of a Jenkins job configuration. These options help control how jobs run, handle secrets, and define exactly what happens during and after a build.

- **Build Environment Options:**
  - **Delete Workspace Before Build Starts:**
    - Cleans the workspace before each job run to avoid leftover files.
  - **Use Secret Text(s) or File(s):**
    - Injects sensitive information like passwords, certificates, or tokens into jobs at runtime.
    - Secrets are stored securely in Jenkins credentials.
  - **Terminate Build If Stuck:**
    - Prevents jobs from running indefinitely.
    - Set a maximum runtime or deadline.
    - Actions on timeout include: abort, fail build, or update description.

- **Build Steps:**
  - Define the specific actions Jenkins takes during a job.
  - Common build steps:
    - **Execute Windows batch command** (for Windows systems)
    - **Execute shell** (for Mac, Linux, or Docker)
    - **Ant, Gradle, Maven** steps for Java projects
  - You can add multiple build steps and reorder them by dragging.

- **Post-Build Actions:**
  - Additional tasks after the build completes, such as:
    - Archiving build artifacts
    - Triggering another job
    - Sending notification emails
  - Multiple post-build actions can be added and rearranged.

- **Built-in Help:**
  - Question mark icons next to options link to built-in documentation for more information.

<!-- FooterStart -->
---
[← 02_04 Build triggers](../02_04_build_triggers/README.md) | [02_06 Run and monitor jobs →](../02_06_run_monitor_jobs/README.md)
<!-- FooterEnd -->
