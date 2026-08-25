# Morning Post -- 2026-08-25

**Topic:** Cloud & DevOps Tips

---

Every junior engineer wastes hours typing the exact same terminal commands every single day...
(with real examples you can use right now)

1. Variables (Store information)
 ↳ What: Save text or numbers into a container so you can reuse them anywhere in your script.
 ↳ Command/Tool: SERVER_NAME="prod-db-01"
 Use Case: When you need to target the same server name multiple times without risk of typos.

2. Automating Backups (Copy with timestamps)
 ↳ What: Create copies of important files dynamically labeled with today's exact date.
 ↳ Command/Tool: cp app.log "app_backup_$(date +%F).log"
 Use Case: When your manager asks for a quick daily snapshot of log files before deployment.

3. Loops (Repeat tasks automatically)
 ↳ What: Run a single command across a list of items without typing it again and again.
 ↳ Command/Tool: for srv in web1 web2 web3; do ping -c 1 $srv; done
 Use Case: When you need to quickly check if 5 microservices are up and running in seconds.

4. Conditional Checks (Make decisions)
 ↳ What: Run a command only if a specific condition is met, like checking if a file exists.
 ↳ Command/Tool: [ -f "/var/log/app.log" ] && echo "File exists"
 Use Case: When your cleanup script should only run if the old log file is actually present.

5. Script Arguments (Accept user input)
 ↳ What: Pass information directly into your script from the terminal when running it.
 ↳ Command/Tool: echo "Deploying application to environment: $1"
 Use Case: When you write one single deployment script that works for dev, staging, or prod.

6. Exit Codes (Catch errors early)
 ↳ What: Stop the script immediately if any command fails so bad things don't happen.
 ↳ Command/Tool: set -e
 Use Case: When you don't want your script deleting files if the previous download step failed.

7. Cron Jobs (Automate scheduling)
 ↳ What: Tell your system to run your Bash script automatically at set times.
 ↳ Command/Tool: 0 2 * * * /home/user/scripts/backup.sh
 Use Case: When you want your backup script to run every single night at 2 AM while you sleep.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by putting 2-3 commands you already run daily into a single script file.
 ↳ Don't forget to make your script executable using chmod +x script.sh before running it.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Bash #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-25/morning/bash-scripting-automate-repetitive-tasks-cheatsheet.pdf

---

*PDF: [bash-scripting-automate-repetitive-tasks-cheatsheet.pdf](bash-scripting-automate-repetitive-tasks-cheatsheet.pdf)*
