# 03_03 Manage artifacts

In this lesson, you'll learn how to manage and archive build artifacts in Jenkins. Artifacts are the files produced by your job, such as executables, reports, or archives, and Jenkins provides tools to make them easy to access after each build.

## Artifacts

In the context of Jenkins, an *artifact* is any file or set of files that a build job produces as its final deliverable. These files capture the tangible outcome of the build and are typically archived, published, or handed off to other jobs for testing, deployment, or analysis.

Examples artifacts include:

- Compiled executables, such as an `.exe` file
- Packaged archives, such as a `.jar` or `.zip` files
- Reports or logs stored saved as `.txt` or `.log` files

Artifacts are stored in the job's workspace during the build.

## Additional Details

- **Locating Artifacts Manually:**
  - You can browse the **Workspace** and locate artifacts by navigating through directories.
  - This is useful, but inefficient for regular use.

- **Archiving Artifacts Automatically:**
  - In the job configuration, under **Post-build Actions**, add **Archive the artifacts**.
  - Specify the file path starting from the top of the workspace.
  - To avoid typing full paths, use wildcards like `**/hello-1.0-SNAPSHOT.jar` to search for the file anywhere in the workspace.

- **Viewing Artifacts After a Build:**
  - After a successful build, a link to the archived artifact appears under the job's workspace.
  - This provides quick, reliable access to build products without browsing the workspace manually.

<!-- FooterStart -->
---
[← 03_02 Browse a job's workspace](../03_02_browse_a_jobs_workspace/README.md) | [03_04 Parameters and environment variables →](../03_04_parameters_environment_variables/README.md)
<!-- FooterEnd -->
