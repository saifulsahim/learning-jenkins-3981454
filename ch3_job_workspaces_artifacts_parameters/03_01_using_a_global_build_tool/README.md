# 03_01 Using a global build tool

## Prerequisites

Configure Git and Maven as a global build tool.

### Git

TODO: Add steps for git

### Maven

In the Jenkins web interface, go to:

`Manage Jenkins` -> `Tools` -> `Maven installations` -> `Add Maven`.

Give your Maven installation a name and check the option to `Install automatically`.

Select the `Save` button.

## Setting up the Jenkins Job

Create a freestyle job and configure it as follows:

1. Under `Source Code Management`, select `Git` and enter the following URL:

    ```bash
    https://github.com/LinkedInLearning/learning-jenkins-3981454
    ```

2. **SET THE `Branch Specifier` to `*/main`**.
3. Add a build step using `Invoke top-level Maven targets`.
4. Select the Maven version you configured in the previous step.
5. For the goal, enter `package`.

### WINDOWS SYSTEMS

After the Maven build step, add a step to run the JAR file.

1. Select `Add build step` -> `Execute Windows batch command`. Enter:

    ```bash
    java -cp target/hello-1.0-SNAPSHOT.jar com.learningjenkins.App
    ```

1. Save the job and start the build.

[Follow this link for more details on running this job on Windows](WINDOWS.md)

## MacOS, Linux, and Docker

After the Maven build step, add a step to run the JAR file.

1. Select `Add build step` -> `Execute shell`. Enter:

    ```bash
    java -cp target/hello-1.0-SNAPSHOT.jar com.learningjenkins.App
    ```

1. Save the job and start the build.

[Follow this link for more details on MacOS, Linux, and Docker](MAC_LINUX_DOCKER.md)

## Troubleshooting Errors

### Make sure Git and Maven are configured

```bash
ERROR:
```

TODO: add steps for troubleshooting Git and Maven

### Check the branch specifier

```bash
ERROR: Couldn't find any revision to build. Verify the repository and branch configuration for this job.
```

Check the branch under Source Code Management.  Enter `*/main` for the branch.

<!-- FooterStart -->
---
[← 02_10 Solution: Automate system monitoring with Jenkins](../../ch2_jenkins_jobs/02_10_solution_automate_system_monitoring_with_jenkins/README.md) | [03_02 Browse a job's workspace →](../03_02_browse_a_jobs_workspace/README.md)
<!-- FooterEnd -->
