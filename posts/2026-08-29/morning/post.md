# Morning Post -- 2026-08-29

**Topic:** Cloud & DevOps Tips

---

Every cloud engineer uses these 7 Linux commands every single day...
(with real examples you can use right now)

1. Searching Text Inside Files
 ↳ What: Find specific keywords or errors hidden inside massive log files.
 ↳ Command/Tool: grep -i "error" app.log
 Use Case: When your app crashes at 3am and you need to find the exact failure reason instantly.

2. Watching Logs Live
 ↳ What: Stream live output from a log file as new events happen.
 ↳ Command/Tool: tail -f /var/log/syslog
 Use Case: When you trigger an API request and want to watch the server process it in real-time.

3. Checking Disk Space
 ↳ What: See how much storage space is left on your server drives.
 ↳ Command/Tool: df -h
 Use Case: When your database suddenly stops saving data because the hard drive is 100% full.

4. Monitoring System Health
 ↳ What: View live CPU usage, memory consumption, and running background processes.
 ↳ Command/Tool: htop
 Use Case: When your boss asks why the application server is running super slow right now.

5. Finding Missing Files
 ↳ What: Search your entire server for files by name, size, or modification date.
 ↳ Command/Tool: find /var/log -name "*.log"
 Use Case: When you know a config file exists somewhere, but you forgot which folder it was saved in.

6. Testing Network Connections
 ↳ What: Check if a web service or API endpoint is responding without opening a browser.
 ↳ Command/Tool: curl -I https://api.example.com
 Use Case: When the frontend team claims the API is down and you need to verify it's live.

7. Fixing File Permissions
 ↳ What: Grant or revoke read, write, and execute rights for files and scripts.
 ↳ Command/Tool: chmod +x deploy.sh
 Use Case: When you try running a new deployment script and get an annoying "Permission denied" error.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start practicing in a safe local Docker container before touching real production servers.
 ↳ Never run destructive commands with sudo unless you fully double-check the path first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Linux #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-29/morning/top-10-linux-commands-youll-use-every-day-at-work-cheatsheet.pdf

---

*PDF: [top-10-linux-commands-youll-use-every-day-at-work-cheatsheet.pdf](top-10-linux-commands-youll-use-every-day-at-work-cheatsheet.pdf)*
