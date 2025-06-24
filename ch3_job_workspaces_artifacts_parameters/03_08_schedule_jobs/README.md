# 03_08 Schedule jobs

In this lesson, you'll learn how to schedule Jenkins jobs to run automatically using cron-style expressions or convenient aliases. Scheduling jobs helps automate routine tasks like updates, system checks, or data processing.

## **Why Schedule Jobs:**

- Automates routine tasks such as software updates, system monitoring, or data downloads.

## **Jenkins Scheduling Format (Cron-Style):**

```python
  ┌───────────────────── 1. minute (0 - 59)
  │ ┌─────────────────── 2. hour (0 - 23)
  │ │ ┌───────────────── 3. day of the month (1 - 31)
  │ │ │ ┌─────────────── 4. month (1 - 12)
  │ │ │ │ ┌───────────── 5. day of the week (0 - 6) (Sunday to Saturday)
  * * * * *
```

- The schedule uses five fields:
    1. Minute (0-59)
    2. Hour (0-23)
    3. Day of the month (1-31)
    4. Month (1-12)
    5. Day of the week (0-7; both 0 and 7 represent Sunday)
- Use an asterisk `*` to represent "any value" for a field.

- **Example Schedules:**
  - `0 0 * * *` — Run at midnight every day.
  - Jenkins suggests replacing specific values like `0` with `H` (hash) to distribute job start times, avoiding bottlenecks.
  - `H H * * *`  — Run at midnight every day using a hashed schedule.

- **Aliases for Convenience:**
  - `@hourly` — Runs once every hour.
  - `@daily` — Runs once every day.
  - `@monthly` — Runs once every month.
  - `@midnight` — Runs sometime between 12 AM and 3 AM (ideal for overnight tasks).

- **Time Zone Considerations:**
  - Schedules follow the time zone of the Jenkins server (often UTC).
  - You can add a time zone specifier for clarity, e.g.:

    ```bash
    TZ=Europe/London
    * * * * *
    ```

  - This runs the job every minute based on London time.

- **Helpful Features:**
  - Jenkins provides feedback showing when the job last ran and when it will run next.
  - Inline help with examples is available by selecting the **?** icon next to the schedule field.

- **Confirming the Schedule Works:**
  - After saving your schedule, wait for builds to trigger automatically.
  - Console output will show the job was **Started by timer**, confirming the job ran as scheduled.

<!-- FooterStart -->
---
[← 03_07 Boolean parameters](../03_07_boolean_parameters/README.md) | [03_09 Challenge Use a Build Tool and Parameters →](../03_09_challenge_use_a_build_tool_parameters/README.md)
<!-- FooterEnd -->
