# ⚙️ Laboratory 09 – Cloud Automation Engineer

## 🚀 Mission Overview

This laboratory activity focuses on automating cloud operations using Bash scripting and Cron scheduling. I created a backup script that compresses application data into a `.tar.gz` file and configured a Cron job to schedule the backup every day at 2:00 AM.

## 🎯 Objectives

- Understand the basic syntax of Bash scripting.
- Create a dummy application directory and a test file.
- Write a script to automatically compress and back up files.
- Use `chmod +x` to make the script executable.
- Configure a Cron job to schedule automatic backups.
- Document the process in GitHub using Markdown.

## 🧰 Tools Used

- KillerCoda Ubuntu Playground
- Bash Shell
- Nano Text Editor
- Linux Cron Scheduler
- GitHub

## 💻 Commands Executed

| Command | Purpose |
|---|---|
| `mkdir app-data` | Creates the application data directory |
| `echo "This is critical client data." > app-data/data.txt` | Creates a sample data file |
| `nano backup.sh` | Creates and edits the backup script |
| `cat backup.sh` | Displays the script contents |
| `chmod +x backup.sh` | Gives the script execution permission |
| `./backup.sh` | Runs the backup script |
| `ls -l backups/` | Verifies the generated backup file |
| `crontab -l` | Displays the scheduled Cron jobs |
| `env EDITOR=nano crontab -e` | Opens the Cron table for editing |

## 🧠 Skills Learned

- Writing and understanding Bash scripts
- Using variables in automation
- Managing Linux file permissions
- Compressing files using the `tar` command
- Scheduling tasks with Cron
- Verifying backup files and documenting technical work

---

<p align="center">
  <b>CCM101 · CLOUD COMPUTING</b><br/>
  <sub>Laboratory 08 — The Cloud Security Engineer</sub>
</p>
