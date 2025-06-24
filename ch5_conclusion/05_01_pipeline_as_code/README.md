# 05_01 Pipeline as code

In this lesson, you'll learn how Jenkins pipelines allow you to configure jobs as code.

Pipelines use a text-based configuration called a **Jenkinsfile**, making it easy to version, share, and maintain your CI/CD processes.

- **What Is a Pipeline:**
  - A pipeline is a Jenkins job defined entirely as code.
  - The configuration lives in a file called a `Jenkinsfile`.
  - Jenkinsfiles are plain text, so they can be stored alongside your project code in a version control system (e.g., GitHub).

- **Benefits of Pipelines:**
  - Store job configuration in source control.
  - Apply versioning and collaboration to your CI/CD process.
  - Easier to read, update, and troubleshoot than manual configurations.

- **Pipeline Structure:**
  - **Stages:** Divide the pipeline into logical sections (e.g., `test`, `build`, `deploy`).
  - **Steps:** Define specific commands or actions for each stage (e.g., checkout code, run tests, build artifacts).

- **Example - Java Calculator Pipeline:**
  - Open the repository for the [Java Calculator project](https://github.com/managedkaos/java-calculator.git).
  - The [`Jenkinsfile`](https://github.com/managedkaos/java-calculator/blob/main/Jenkinsfile) defines parameters, build steps (Maven commands), and post-build actions (archive JAR file, test results).
  - On **Windows** systems, please refer to the [Windows.Jenkinsfile](https://github.com/managedkaos/java-calculator/blob/main/Windows.Jenkinsfile)
  - After running the pipeline, you can:
    - View the stages and their pass/fail status.
    - Drill down into each stage to see detailed output for each step.

<!-- FooterStart -->
---
[← 04_07 Solution Create Folders and Views](../../ch4_organize_jobs_with_views_folders/04_07_solution_create_folders_views/README.md) | [05_02 Build agents and cloud runners →](../05_02_jenkins_build_agents_cloud_runners/README.md)
<!-- FooterEnd -->
