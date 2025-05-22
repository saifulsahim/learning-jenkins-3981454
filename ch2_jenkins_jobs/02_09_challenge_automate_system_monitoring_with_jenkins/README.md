# 02_09 Challenge: Automate system monitoring with Jenkins

In this challenge you will create a report with details on the system where Jenkins is running.

## **Challenge Overview**

1. Create a freestyle job named `system-report`.
2. Configure the job to automatically run once a day using a schedule.
3. Add a build step that runs a provided script with commands that check the status of the system.
   1. *Note: Use the commands that are specific to the platform where your Jenkins installation is running.*
4. Archive the results of the build step using the target  Record the output of the commands in a report named `system-report.txt`.
5. Run the job manually to confirm the script runs as expected and the results are archived.

## **Instructions**

1. **Create a freestyle Job**

   - Name the job `system-report`.

2. **Add a build trigger**

   - Schedule the job to run once a day. Options include the following, among others:
     - `0 0 * * *`
     - `H H * * *`
     - `@daily`
     - `@midnight`

3. **Configure a platform-specific build step**

   - **Windows:** Add a build step using **Execute Windows batch command** with the following script:

      ```bat
      @echo off
      set REPORT_FILE=system-report.txt
      echo System Report - %DATE% %TIME% > %REPORT_FILE%
      echo. >> %REPORT_FILE%

      echo Disk Usage: >> %REPORT_FILE%
      wmic logicaldisk get caption,freespace,size >> %REPORT_FILE%
      echo. >> %REPORT_FILE%

      echo Memory Status: >> %REPORT_FILE%
      systeminfo | findstr /C:"Total Physical Memory" /C:"Available Physical Memory" >> %REPORT_FILE%
      echo. >> %REPORT_FILE%

      echo Running Processes: >> %REPORT_FILE%
      tasklist >> %REPORT_FILE%
      echo. >> %REPORT_FILE%

      echo Logged-in Users: >> %REPORT_FILE%
      query user >> %REPORT_FILE%
      ```

   - **macOS, Linux, and Docker:** Add a build step using **Execute shell** with the following script:

      ```bash
      #!/bin/bash

      REPORT_FILE="system-report.txt"
      echo "System Report - $(date)" > $REPORT_FILE
      echo "" >> $REPORT_FILE

      echo "Disk Usage:" >> $REPORT_FILE
      df -h >> $REPORT_FILE
      echo "" >> $REPORT_FILE

      echo "Memory Usage:" >> $REPORT_FILE
      free -m >> $REPORT_FILE
      echo "" >> $REPORT_FILE

      echo "Running Processes:" >> $REPORT_FILE
      ps aux --sort=-%mem | head -10 >> $REPORT_FILE
      echo "" >> $REPORT_FILE

      echo "Logged-in Users:" >> $REPORT_FILE
      who >> $REPORT_FILE
      ```

4. **Archive the report**

   - Configure **Post-build Actions** to use **Archive the artifacts** to archive the file `system-report.txt`.

5. **Verify the configuration**

   - Manually trigger the job.
   - Use the **Console Output** and **Artifacts** viewer to verify success.

<!-- FooterStart -->
---
[← 02_08 Monitor build trends](../02_08_monitor_build_trends/README.md) | [02_10 Solution: Automate system monitoring with Jenkins →](../02_10_solution_automate_system_monitoring_with_jenkins/README.md)
<!-- FooterEnd -->
