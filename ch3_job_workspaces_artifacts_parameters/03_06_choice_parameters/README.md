# 03_06 Choice parameters

Create a freestyle job with one build step.

Add a choice parameter named `ENVIRONMENT` with three or more choices.

## WINDOWS SYSTEMS

If you are running Jenkins on a Windows system:

1. Select the `Execute Windows batch command` build step
2. Enter the following for the command:

```cmd
@echo off
@echo ENVIRONMENT = %ENVIRONMENT%
```

[Follow this link for more details on Windows.](WINDOWS.md)

## MacOS, Linux, and Docker

If you are running Jenkins on MacOS, Linux, or Docker:

1. Select the `Execute shell` build step.
2. Enter the following for the command:

```bash
#!/bin/bash
echo "ENVIRONMENT = $ENVIRONMENT"
```

[Follow this link for more details on MacOS, Linux, and Docker.](MAC_LINUX_DOCKER.md)

<!-- FooterStart -->
---
[← 03_05 String parameters](../03_05_string_parameters/README.md) | [03_07 Boolean parameters →](../03_07_boolean_parameters/README.md)
<!-- FooterEnd -->
