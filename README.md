# Automations for Codex App

This repository contains a collection of automation scripts and configurations for Codex App.

## Installation

To start using these automations, simply copy the files to the following path:

`~/.codex/automations`

(Expand `~` to your home directory, e.g., `/Users/yourusername/.codex/automations` in macOS)

## Configuration

After copying the files, please open the `automation.toml` files and update the `cwds` field to point to your actual project path:

```toml
cwds = ["/path/to/project"]  # <--- Change this to your project path
```

## Schedule Configuration

The `rrule` field in `automation.toml` controls the schedule of the automation using standard iCalendar RRULE format.

**Common Parameters:**

- **FREQ**: Frequency (e.g., `WEEKLY`, `HOURLY`)
- **INTERVAL**: Repetition interval (e.g., `2` for every 2 hours)
- **BYHOUR**: Hour of the day (0-23)
- **BYMINUTE**: Minute of the hour (0-59)
- **BYDAY**: Days of the week (`MO`, `TU`, `WE`, `TH`, `FR`, `SA`, `SU`)

**Examples:**

- **Weekly on Fridays at 4 PM:**
  `FREQ=WEEKLY;BYHOUR=16;BYMINUTE=0;BYDAY=FR`

- **Daily (Mon-Fri) at 9:30 AM:**
  `FREQ=WEEKLY;BYHOUR=9;BYMINUTE=30;BYDAY=MO,TU,WE,TH,FR`

- **Every 2 hours on weekdays:**
  `FREQ=HOURLY;INTERVAL=2;BYMINUTE=0;BYDAY=MO,TU,WE,TH,FR`

## Available Automations

The following automations are included:

- **1. Daily Bug Scan**: Scan recent commits for likely bugs.
- **2. Weekly Release Notes**: Draft weekly release notes from merged PRs.
- **3. Standup Summary**: Summarize yesterday's git activity.
- **4. Nightly CI Report**: Summarize CI failures and flaky tests.
- **5. Daily Classic Game**: Create a small classic game with minimal scope.
- **6. Skill Progression Map**: Suggest next skills to deepen based on PRs.
- **7. Weekly Engineering Summary**: Synthesize the week's engineering activities.
- **8. Performance Regression Watch**: Compare recent changes to benchmarks.
- **9. Dependency and SDK Drift**: Detect dependency drift.
- **10. Test Gap Detection**: Identify untested paths from recent changes.
- **11. Pre-release Check**: Verify changelog, migrations, etc., before tagging.
- **12. Update Agents MD**: Update AGENTS.md with new workflows.
- **13. Weekly PR Summary**: Summarize last week's PRs.
- **14. Issue Triage**: Triage new issues.
- **15. CI Monitor**: Check CI failures.
- **16. Dependency Sweep**: Scan outdated dependencies.
- **17. Performance Audit**: Audit performance regressions.
- **18. Update Changelog**: Update the changelog with this week's highlights.
