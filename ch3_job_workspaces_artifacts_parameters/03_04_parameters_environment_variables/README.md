# 03_04 Parameters and environment variables

In this lesson, you'll learn how to make your Jenkins jobs more flexible by using parameters and environment variables. Parameters allow users to provide values at runtime, and those values can be accessed throughout your job configuration.

## **Using Parameters**

- Makes jobs reusable for different situations by accepting input at build time.
- Supported parameter types include:
  - **String**
  - **Choice** (drop-down options)
  - **Boolean** (True/False)

- Parameter names are **case sensitive** on Mac, Linux, and Docker but **not** on Windows.

- Use all-uppercase, consistent, and simple names without spaces or special characters.

## **WINDOWS SYSTEMS**

If you are running Jenkins on a Windows system, use variables with this format:

**`%VARIABLE_NAME%`**

## MacOS, Linux, and Docker

If you are running Jenkins on MacOS, Linux, or Docker, use variables with this format:

**`$VARIABLE_NAME`**

## **Example Job Setup**

- Create a **freestyle job** named `parameterized-job-example`.
- Add these parameters:
  - `STRING_PARAMETER` (default value: `APA1906`)
  - `CHOICE_PARAMETER` (options: `ALPHA`, `GAMMA`, `OMEGA`)
  - `BOOLEAN_PARAMETER` (default: `True`)

- **Accessing Parameters with Environment Variables:** After adding your parameters, scroll down to the **Build** section of the job configuration.
  - Click **Add build step**, then choose the appropriate option based on your system:
    - For **Windows** systems, select **Execute Windows batch command**.
    - For **Mac, Linux, or Docker** systems, select **Execute shell**.

  - Inside the command field, you can reference your parameters as environment variables.

  - On **Windows** (Batch commands):

    ```bat
    echo %STRING_PARAMETER%
    echo %CHOICE_PARAMETER%
    echo %BOOLEAN_PARAMETER%
    ```

  - On **Mac, Linux, Docker** (Shell):

    ```bash
    echo $STRING_PARAMETER
    echo $CHOICE_PARAMETER
    echo $BOOLEAN_PARAMETER
    ```

  - These commands will print the values of the parameters to the console output when the job runs, allowing you to verify they were passed in correctly.

## **Jenkins Built-In Environment Variables:**

- Access additional environment variables provided by Jenkins via the **See the list of available environment variables** link in the build step configuration.
- Common examples:
  - `BUILD_ID`
  - `BUILD_NUMBER`
- These are useful for tasks like tagging artifacts with build information.

<!-- FooterStart -->
---
[← 03_03 Manage artifacts](../03_03_manage_artifacts/README.md) | [03_05 String parameters →](../03_05_string_parameters/README.md)
<!-- FooterEnd -->
