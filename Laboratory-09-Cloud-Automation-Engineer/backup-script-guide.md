# Backup Script Technical Guide

## 1. Purpose

The backup script automates the process of compressing application data into a `.tar.gz` archive. It creates the backup directory when needed and adds a timestamp to each backup filename.

## 2. Complete Bash Script

The script is stored at `/root/backup.sh`.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

## 3. Executable Permissions

The command `chmod +x /root/backup.sh` grants executable permission to the script. This allows it to be run directly with `/root/backup.sh` or `./backup.sh` from the root directory.

## 4. Cron Job Configuration

The Cron entry used in this activity is:

```cron
0 2 * * * /root/backup.sh
```

This entry schedules the script to run every day at 2:00 AM, according to the system's local time.

## 5. The Five Cron Fields

| Field | Value | Explanation |
|---|---|---|
| Minute | `0` | Runs at minute zero |
| Hour | `2` | Runs at 2 AM |
| Day of Month | `*` | Runs every day of the month |
| Month | `*` | Runs every month |
| Day of Week | `*` | Runs every day of the week |

## 6. Verification Commands

- `chmod +x /root/backup.sh` — grants executable permission.
- `/root/backup.sh` — runs the backup script.
- `ls -lh /root/backups/` — lists the generated backup archives.
- `tar -tzf /root/backups/backup_*.tar.gz` — checks the archive contents.
- `crontab -l` — displays the installed Cron schedule.

The archive should contain `app-data/data.txt`, confirming that the sample application data was included in the backup.
