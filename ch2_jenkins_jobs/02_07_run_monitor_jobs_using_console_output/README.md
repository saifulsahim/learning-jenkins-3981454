# 02_07 Run and monitor jobs using console output

In this lesson, you'll learn how to monitor your Jenkins jobs using the console output. You'll see how to follow real-time output, interpret build results, and simulate failures to better understand how Jenkins reports job status.

- **Viewing Console Output:**
  - Select the pull-down menu next to a build number and choose **Console Output**, or
  - Click the checkmark next to a completed build to view output details.
  - Console output shows:
    - Who ran the build
    - Where it ran
    - The output produced during the build

- **Real-Time Output:**
  - Start a new build by selecting **Build Now**.
  - Click the checkmark next to the running job to open live console output.
  - The console updates automatically as the job runs, with automatic scrolling.

- **Simulating a Build Failure:**
  - Edit the job configuration under **Build Steps**.
  - Add a command at the end of the step to force a failure:
    - **For Unix/Linux/Docker:** `exit 1`
    - **For Windows (Batch):** `exit /b 1`
    - **For Windows (PowerShell):** `exit 1`
  - Save and run the job—Jenkins will report a **FAILURE** status.
  - Visual indicators of failure include:
    - A red **X** next to the build
    - A red **X** at the top of the console output

- **Fixing the Job:**
  - Remove the failing command from the build step to restore normal operation.

<!-- FooterStart -->
---
[← 02_06 Run and monitor jobs](../02_06_run_monitor_jobs/README.md) | [02_08 Monitor build trends →](../02_08_monitor_build_trends/README.md)
<!-- FooterEnd -->
