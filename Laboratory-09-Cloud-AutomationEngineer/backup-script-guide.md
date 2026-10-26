# Backup Script Technical Guide

## 1. Backup Script Code

The following Bash script creates a backup directory and compresses the application data into a `.tar.gz` file with a timestamp in its filename.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## 2. File Permissions

The command `chmod +x backup.sh` gives the script permission to execute as a program. Without this permission, running `./backup.sh` resulted in a "Permission denied" error. After changing the permission, the script ran successfully and created the compressed backup file.

## 3. Cron Job Configuration

The Cron expression used was:

```bash
0 2 * * * /root/backup.sh
```

This schedules the backup script to run every day at 2:00 AM.

### Meaning of the Five Time Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At minute zero |
| Hour | `2` | At 2 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

The final part, `/root/backup.sh`, is the absolute path to the script that Cron executes.

## 4. Verification

The script was tested in the KillerCoda Ubuntu terminal. It successfully created the `backups` directory and generated the file `backup_20261026_125913.tar.gz`.

The Cron configuration was verified using `crontab -l`, which displayed the scheduled command.

---
<p align="center">
  <b>CCM101 · CLOUD COMPUTING</b><br/>
  <sub>Laboratory 09 – Cloud Automation Engineer</sub>
</p>
