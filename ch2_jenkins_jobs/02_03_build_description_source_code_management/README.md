# 02_03 Build description and source code management

In this lesson, you'll learn how to document your Jenkins jobs with descriptions, manage old builds to save space, and connect your jobs to source code repositories using Git. These foundational settings help keep your jobs organized and efficient.

- **General Section:**
  - **Description Field:**
    - Add free-form text to describe the job and its purpose.
    - Useful for providing details beyond the job name.
  - **Discard Old Builds:**
    - Controls how long build records and files are retained.
    - You can set a maximum number of builds or days to keep builds.
    - The **Advanced** button provides additional options, such as controlling how long artifacts are kept.

- **Source Code Management (SCM) Section:**
  - Enables Jenkins to interact with code stored in repositories.
  - Selecting **Git** allows you to:
    - Enter the repository URL.
    - Add credentials for private repositories.
    - Specify branches to check out.
  - This lets Jenkins pull code from external repositories (e.g., GitHub, GitLab, Bitbucket) into the job workspace for integration, testing, or deployment.

<!-- FooterStart -->
---
[← 02_02 Job types](../02_02_job_types/README.md) | [02_04 Build triggers →](../02_04_build_triggers/README.md)
<!-- FooterEnd -->
