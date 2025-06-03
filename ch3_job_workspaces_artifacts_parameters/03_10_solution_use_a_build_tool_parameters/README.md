# 03_10 Solution Use a Build Tool and Parameters

In this challenge, you’ll create a Jenkins job that uses tools to build a Java-based application.

## **Challenge Overview**

1. Configured Maven and Git under **Manage Jenkins → Tools**.
2. Create a freestyle job named `java-calculator`.
3. Configure the job to:
   1. use parameters
   2. fetch code from a Git repository
   3. build the application with Maven
   4. run the Java application
   5. and archive the JAR and test result artifacts.

This challenge should take 10 to 15 minutes to complete.

## **Instructions**

1. **Install tools**

   - Navigate to **Manage Jenkins → Tools**.
   - If you're using **Windows**, specify the path to your system’s `git.exe` under **Git installations, Path to Git executable**.
   - Install the latest version of **Apache Maven.** Include the version number in the installation name.  For example, **Maven 3.9.9** should be named `maven-3.9.9`.

2. **Create a freestyle project**

   - Name the project: `java-calculator`.

3. **Add build parameters**

   - Add a **Choice Parameter** named `OPERATION` with the following options:

     - `add`
     - `subtract`
     - `multiply`
     - `divide`

   - Add two **String Parameters** with the following names and default values:

     - `NUMBER_1`; For default value use `10`
     - `NUMBER_2`; For default value use `5`

4. **Configure source code management**

   - Use Git.
   - For **Repository URL**, enter `https://github.com/managedkaos/java-calculator.git`
   - Set the **Branch Specifier** to `*/main`.

5. Add a build step using **"Invoke top-level Maven targets"** with the following configuration:

   - **Maven Version** with the Maven installation previously configured
   - **Goals** should be: `clean test package`

6. **Configure a platform-specific build step**
   - **Windows:** Add a build step using **Execute Windows batch command** with the following script:

     ```bat
     @echo off
     echo         Build: %BUILD_ID%
     echo     Operation: %OPERATION%
     echo  First number: %NUMBER_1%
     echo Second number: %NUMBER_2%
     java -jar target\calculator-1.0-SNAPSHOT.jar %OPERATION% %NUMBER_1% %NUMBER_2%
     ```

   - **macOS, Linux, and Docker:** Add a build step using **Execute shell** with the following script:

     ```bash
     #!/bin/bash
     echo "        Build: $BUILD_ID"
     echo "    Operation: $OPERATION"
     echo " First number: $NUMBER_1"
     echo "Second number: $NUMBER_2"
     java -jar target/calculator-1.0-SNAPSHOT.jar $OPERATION $NUMBER_1 $NUMBER_2
     ```

7. Add the following **Post-Build Actions:**

   - **Archive the artifacts** with **Files to archive**  set to `**/target/calculator-1.0-SNAPSHOT.jar`
   - **Publish JUnit test result report** with **Test report XMLs** set to `**/target/surefire-reports/*.xml`

8. **Verify the configuration**

   - Manually trigger the job.
   - Use the **Console Output** and **Artifacts** viewer to verify success.

<!-- FooterStart -->
---
[← 03_09 Challenge Use a Build Tool and Parameters](../03_09_challenge_use_a_build_tool_parameters/README.md) | [04_01 Views and folders →](../../ch4_organize_jobs_with_views_folders/04_01_views_folders/README.md)
<!-- FooterEnd -->
