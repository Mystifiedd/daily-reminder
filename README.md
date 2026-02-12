# daily-reminder

GitHub Actions-powered daily reminder bot with exam schedule &amp; ITRI internship goals

## 📋 Overview

This repository contains an automated daily reminder system built with GitHub Actions. It sends daily reminders about:
- 📚 Exam schedules and study materials
- 💼 ITRI internship goals and progress tracking

## 🚀 Features

- **Automated Daily Reminders**: Runs every day at 8:00 AM UTC (1:45 PM Nepal Time)
- **Manual Trigger**: Run the workflow on-demand whenever needed
- **Summary Artifacts**: Downloads reminder checklists as artifacts
- **Exam Schedule Reminders**: Never miss important study tasks
- **ITRI Internship Tracking**: Stay on top of your internship goals

## 📊 Workflow Status

[![Daily Reminder](https://github.com/Mystifiedd/daily-reminder/actions/workflows/daily-reminder.yml/badge.svg)](https://github.com/Mystifiedd/daily-reminder/actions/workflows/daily-reminder.yml)

**Current Status**: ✅ Active and configured

For detailed status information, see [WORKFLOW_STATUS.md](WORKFLOW_STATUS.md)

## 🎯 How to Use

### View Reminders
1. Go to the [Actions tab](https://github.com/Mystifiedd/daily-reminder/actions)
2. Click on the latest "Daily Reminder" workflow run
3. View the job logs to see your daily reminders

### Manual Trigger
1. Navigate to [Actions > Daily Reminder](https://github.com/Mystifiedd/daily-reminder/actions/workflows/daily-reminder.yml)
2. Click "Run workflow"
3. Select your branch and click "Run workflow"

### Download Reminder Checklist
1. Open any workflow run
2. Scroll to the "Artifacts" section
3. Download the reminder summary markdown file

## 📅 Schedule

The workflow runs automatically:
- **Daily at**: 8:00 AM UTC (1:45 PM NPT)
- **Frequency**: Once per day
- **Can also be triggered manually** at any time

## 📖 Documentation

- [Workflow Status Report](WORKFLOW_STATUS.md) - Detailed workflow status and configuration
- [Daily Reminder Workflow](.github/workflows/daily-reminder.yml) - The actual workflow file

## 🔧 Customization

To customize the reminder content or schedule:
1. Edit `.github/workflows/daily-reminder.yml`
2. Modify the reminder messages in the workflow steps
3. Change the cron schedule if needed (use [crontab.guru](https://crontab.guru/) for help)

## 📝 License

This project is open source and available for educational purposes.
