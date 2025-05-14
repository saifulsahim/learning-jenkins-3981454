# 02_06 Run and monitor jobs

Create a freestyle job with one build step.

## WINDOWS SYSTEMS

If you are running Jenkins on a Windows system:

1. Select the `Execute Windows batch command` build step
1. Enter one of the following for the command:

```batch
@echo off
for /L %%i in (1,1,30) do (
  @echo %%i
  @timeout /t 1 /nobreak > NUL
)
```

```powershell
powershell.exe -Command "for ($i = 1; $i -le 30; $i++) { Write-Host $i; Start-Sleep -Seconds 1 }"
```

[Follow this link for more details on Windows](WINDOWS.md)

## MacOS, Linux, and Docker

If you are running Jenkins on MacOS, Linux, or Docker:

1. Select the `Execute shell` build step.
1. Enter the following for the command:

```
#!/bin/bash
for i in {1..30}; do
  echo $i;
  sleep 1;
done
```

[Follow this link for more details on MacOS, Linux, and Docker](MAC_LINUX_DOCKER.md)

<!-- FooterStart -->
---
[← 02_05 The build environment](../02_05_the_build_environment/README.md) | [02_07 Run and monitor jobs using console output →](../02_07_run_monitor_jobs_using_console_output/README.md)
<!-- FooterEnd -->
