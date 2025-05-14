# 03-06: Choice Parameters with Windows

Create a freestyle job with one build step.

Add a choice parameter with three or more choices.

## WINDOWS SYSTEMS

If you are running Jenkins on a Windows system:

1. Select the `Execute Windows batch command` build step
2. Enter the following for the command:

```cmd
@echo off
@echo ENVIRONMENT = %ENVIRONMENT%
```

## Troubleshooting Errors
