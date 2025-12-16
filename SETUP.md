# LeetCode Daily Automation Setup Guide

## Overview
This GitHub Actions workflow automatically runs an easy LeetCode problem solver daily at **22:50 IST**.

## Features
✅ Automated daily execution at 22:50 IST
✅ Runs on GitHub servers (no local machine needed)
✅ Selenium-based browser automation
✅ Logs all submissions
✅ Easily customizable schedule

## What's Included

### Files
- `.github/workflows/leetcode-daily.yml` - GitHub Actions workflow
- `leetcode_solver.py` - Main automation script
- `requirements.txt` - Python dependencies
- `SETUP.md` - This setup guide

## How It Works

1. **Scheduled Trigger**: GitHub Actions runs the workflow daily at 22:50 IST
2. **Environment Setup**: Python and Chrome drivers are installed
3. **Execution**: The Python script navigates to LeetCode and solves an easy problem
4. **Logging**: Results are logged to `submissions.log`
5. **Commit**: Changes are automatically committed to the repository

## Cron Expression Explained

The workflow runs on cron schedule: `20 17 * * *`
- This is **17:20 UTC** (equivalent to 22:50 IST)
- IST is UTC+5:30, so 22:50 IST - 5:30 = 17:20 UTC
- Format: `minute hour day month day_of_week`

## Modifying the Schedule

To change the daily execution time:
1. Edit `.github/workflows/leetcode-daily.yml`
2. Modify the cron expression
3. Commit the changes

### Example Time Conversions
- **18:00 IST** → `12:30 UTC` → `cron: '30 12 * * *'`
- **20:00 IST** → `14:30 UTC` → `cron: '30 14 * * *'`
- **23:30 IST** → `18:00 UTC` → `cron: '0 18 * * *'`

## Enabling/Disabling

### To Enable
- Simply push changes to the repository
- GitHub Actions will activate automatically

### To Disable
- Comment out the `schedule` section in `.github/workflows/leetcode-daily.yml`

## Monitoring Execution

To see workflow runs:
1. Go to your repository
2. Click on **Actions** tab
3. Select **Daily LeetCode Easy Problem Solver**
4. View run logs and status

## Troubleshooting

**Workflow not running?**
- Check that GitHub Actions is enabled in repository settings
- Verify the cron schedule is correct
- Check workflow file syntax

**Script errors?**
- Review the Actions logs
- Check if Selenium/webdriver-manager dependencies are properly installed
- Verify LeetCode website structure hasn't changed

## Next Steps

1. ✅ Repository created
2. ✅ Workflow file added
3. ✅ Python script added
4. ✅ Dependencies configured
5. 🎯 Workflow will start running automatically!

## Important Notes

- The automation runs on GitHub's Ubuntu servers
- No credit card required (free tier)
- Logs are saved in `submissions.log`
- You can manually trigger runs from the Actions tab

---

**Created for daily LeetCode practice automation!** 🚀
