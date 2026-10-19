# Mission 9: The Cloud Automation Engineer

## Mission Overview

This laboratory activity focuses on using Bash scripting and Cron to automate data backups. A sample application directory was created, and a script was written to compress its contents into a timestamped archive. A Cron job was also configured to run the backup automatically every day at 2:00 AM.

## Objectives

- Understand basic Bash scripting and variables.
- Create and execute an automated backup script.
- Apply executable permissions using `chmod`.
- Compress application data into a `.tar.gz` archive.
- Configure a recurring Cron job.
- Document the implementation using Markdown.

## Commands Executed

```bash
mkdir -p app-data
echo "This is critical client data." > app-data/data.txt
nano /root/backup.sh
chmod +x /root/backup.sh
/root/backup.sh
ls -lh /root/backups/
tar -tzf /root/backups/backup_*.tar.gz
crontab -l
env EDITOR=nano crontab -e
```

## Skills Learned

This activity provided practice in writing Bash scripts, managing files and directories, setting executable permissions, and creating compressed backups. It also demonstrated how Cron can schedule routine tasks without requiring manual execution. Testing the script and checking the archive helped demonstrate the importance of verifying automated processes.

## Evidence

The following required screenshots will be uploaded manually to the `screenshots/` directory:

- `script-execution.png` — successful backup execution and archive.
- `cron-schedule.png` — installed Cron schedule.
