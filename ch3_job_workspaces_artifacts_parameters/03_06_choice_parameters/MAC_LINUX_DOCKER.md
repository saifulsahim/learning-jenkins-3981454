# 03-06: Choice Parameters with MacOS, Linux, and Docker

Create a freestyle job with one build step.

Add a choice parameter named `ENVIRONMENT` with three or more choices.

## MacOS, Linux, and Docker

If you are running Jenkins on MacOS, Linux, or Docker:

1. Select the `Execute shell` build step.
2. Enter the following for the command:

```bash
#!/bin/bash
echo "ENVIRONMENT = $ENVIRONMENT"
```

## Troubleshooting Errors
