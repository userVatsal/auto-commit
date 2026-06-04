# 🟩 auto-commit

Keeps the GitHub contribution graph green every day — automatically, for free.

## How it works

A GitHub Actions workflow runs on a daily cron schedule (`0 0 * * *` — midnight UTC).  
It appends a timestamped line to `log.txt`, commits, and pushes. That's it.

## Setup

1. Create this repo on GitHub (public or private — both work)
2. Go to **Settings → Actions → General → Workflow permissions**
3. Select **Read and write permissions** → Save
4. Push these files — the workflow activates immediately

To trigger it manually: **Actions → 🟩 Daily Commit → Run workflow**

## Customise the time

Edit the cron expression in `.github/workflows/daily-commit.yml`:

```yaml
- cron: '0 9 * * *'   # 9am UTC daily
- cron: '0 12 * * *'  # noon UTC daily
```

Use [crontab.guru](https://crontab.guru) to build your own schedule.
