# 03_05 String parameters

Create a freestyle job with one build step.

Add a string parameter for `VERSION_NUMBER`.

## WINDOWS SYSTEMS

If you are running Jenkins on a Windows system:

1. Select the `Execute Windows batch command` build step
2. Enter the following for the command:

```cmd
@echo off
@echo VERSION_NUMBER = %VERSION_NUMBER%
```

[Follow this link for more details on Windows.](WINDOWS.md)

## MacOS, Linux, and Docker

If you are running Jenkins on MacOS, Linux, or Docker:

1. Select the `Execute shell` build step.
2. Enter the following for the command:

```bash
#!/bin/bash
echo "VERSION_NUMBER = $VERSION_NUMBER"
```

<!-- FooterStart -->
---
[← 03_04 Parameters and environment variables](../03_04_parameters_environment_variables/README.md) | [03_06 Choice parameters →](../03_06_choice_parameters/README.md)
<!-- FooterEnd -->
