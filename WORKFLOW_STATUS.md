# Daily Reminder Workflow Status

## Overview
This document provides the status and details of the daily-reminder GitHub Actions workflow for the Mystifiedd/daily-reminder repository.

## Workflow Details

### Name
**Daily Reminder**

### Location
`.github/workflows/daily-reminder.yml`

### Status
✅ **Active** - The workflow has been created and is configured to run automatically.

### Schedule
- **Cron Schedule**: `0 8 * * *`
- **Time**: 8:00 AM UTC daily (approximately 1:45 PM Nepal Time)
- **Frequency**: Once per day

### Triggers
1. **Scheduled**: Runs automatically at 8:00 AM UTC every day
2. **Manual**: Can be triggered manually via `workflow_dispatch`

## Workflow Features

### 1. Daily Reminder Messages
The workflow displays motivational messages and reminders including:
- 📅 Current date and time
- 📚 Exam Schedule Reminders
  - Check exam schedule
  - Review study materials
  - Complete pending assignments
- 💼 ITRI Internship Goals
  - Track daily progress
  - Review project milestones
  - Complete assigned tasks
  - Document learnings

### 2. Reminder Summary Artifact
- Creates a markdown file with a checklist format
- Uploaded as a workflow artifact
- Retention period: 7 days
- Artifact name format: `daily-reminder-YYYYMMDD`

## Current Workflow Configuration

```yaml
name: Daily Reminder

on:
  schedule:
    - cron: '0 8 * * *'
  workflow_dispatch:

jobs:
  send-reminder:
    runs-on: ubuntu-latest
    steps:
      - Checkout repository
      - Send Daily Reminder
      - Create reminder summary
      - Upload reminder artifact
```

## How to Use

### Manual Trigger
1. Go to the [Actions tab](https://github.com/Mystifiedd/daily-reminder/actions)
2. Select "Daily Reminder" workflow
3. Click "Run workflow"
4. Select the branch and click "Run workflow"

### View Reminder Output
1. Navigate to [Actions](https://github.com/Mystifiedd/daily-reminder/actions)
2. Click on a workflow run
3. View the job logs to see the reminder messages
4. Download the artifact for a formatted checklist

## Workflow Runs

### Expected Behavior
- Runs automatically every day at 8:00 AM UTC
- Can be manually triggered at any time
- Creates logs with reminder messages
- Uploads a markdown summary as an artifact

### Monitoring
To check the workflow status:
1. Visit the [Actions tab](https://github.com/Mystifiedd/daily-reminder/actions/workflows/daily-reminder.yml)
2. Review recent workflow runs
3. Check for any failures or issues

## Technical Details

### Dependencies
- **GitHub Actions**: Uses ubuntu-latest runner
- **Actions Used**:
  - `actions/checkout@v4` - For checking out the repository
  - `actions/upload-artifact@v4` - For uploading reminder summaries

### Resource Usage
- **Compute**: Minimal (< 1 minute per run)
- **Storage**: Artifacts retained for 7 days
- **Cost**: Free tier (well within GitHub Actions limits)

## Future Enhancements

Potential improvements to consider:
1. Integration with GitHub Issues for task tracking
2. Email notifications via GitHub Actions
3. Customizable reminder content via configuration files
4. Integration with calendar APIs for exam schedules
5. Slack/Discord notifications
6. Weekly summary reports

## Maintenance

### Updating the Schedule
To change the reminder time, edit the cron expression in `.github/workflows/daily-reminder.yml`:
```yaml
schedule:
  - cron: '0 8 * * *'  # Modify this line
```

Use [crontab.guru](https://crontab.guru/) to help create cron expressions.

### Modifying Reminder Content
Edit the "Send Daily Reminder" and "Create reminder summary" steps in the workflow file.

## Status Check Summary

✅ **Workflow Created**: Daily Reminder workflow exists in `.github/workflows/daily-reminder.yml`  
✅ **Configuration Valid**: YAML syntax is correct  
✅ **Schedule Configured**: Set to run daily at 8:00 AM UTC  
✅ **Manual Trigger Enabled**: Can be run on-demand via workflow_dispatch  
✅ **Artifacts Configured**: Reminder summaries will be saved for 7 days  
⏳ **First Run Pending**: Waiting for next scheduled run or manual trigger  

---

**Last Updated**: 2026-02-12  
**Workflow Version**: 1.0  
**Maintained By**: Mystifiedd/daily-reminder repository
