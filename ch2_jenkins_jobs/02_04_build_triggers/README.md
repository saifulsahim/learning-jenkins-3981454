# 02_04 Build triggers

In this lesson, you'll learn how to configure different types of triggers to control when your Jenkins jobs start. Triggers allow jobs to run automatically based on schedules, events, or external actions, giving you flexibility and control.

- **Trigger Builds Remotely:**
  - Allows jobs to be started by accessing a URL through the Jenkins web API.
  - Useful for triggering jobs from external scripts or systems.

- **Build After Other Projects Are Built:**
  - Starts a job automatically when other jobs finish.
  - Ideal for chaining jobs together when they depend on each other.

- **Build Periodically:**
  - Runs jobs on a schedule (hourly, daily, weekly, etc.).
  - Uses **Cron format** for precise scheduling.
  - A more detailed lesson on scheduling is provided later in the course.

- **GitHub Hook Trigger for GITScm Polling:**
  - Starts jobs based on activity in GitHub, such as commits, tags, or releases.
  - Requires configuring a webhook in GitHub.
  - Recommended for Continuous Integration workflows.

- **Poll SCM:**
  - Jenkins periodically checks the repository for changes.
  - Less efficient than webhooks—can consume unnecessary system resources.
  - Generally not recommended unless webhooks aren't possible.

<!-- FooterStart -->
---
[← 02_03 Build description and source code management](../02_03_build_description_source_code_management/README.md) | [02_05 The build environment →](../02_05_the_build_environment/README.md)
<!-- FooterEnd -->
