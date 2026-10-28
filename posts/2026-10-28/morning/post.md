# Morning Post -- 2026-10-28

**Topic:** Cloud & DevOps Tips

---

Getting paged at 3 AM for a broken app is every engineer's worst nightmare...
(with real examples you can use right now)

1. Health Checks
 ↳ What: Check if your application endpoint is returning healthy status codes.
 ↳ Command/Tool: curl -I http://localhost:8080/health
 Use Case: When an alert fires saying your web app is unreachable.

2. Live Log Streaming
 ↳ What: Stream live log entries to watch errors happen in real time.
 ↳ Command/Tool: tail -f /var/log/nginx/error.log
 Use Case: When users report errors after you just deployed new code.

3. CPU & Memory Check
 ↳ What: Identify which background process is hogging system resource capacity.
 ↳ Command/Tool: top -o %CPU
 Use Case: When your server slows down and stops responding to traffic.

4. Disk Space Inspection
 ↳ What: Verify if full disk space is crashing your application database.
 ↳ Command/Tool: df -h
 Use Case: When your app suddenly stops saving new user data.

5. Port Connectivity Test
 ↳ What: Test if a specific network port is open and accepting traffic.
 ↳ Command/Tool: nc -zv 127.0.0.1 5432
 Use Case: When your web service cannot connect to your PostgreSQL database.

6. Service Recovery Restart
 ↳ What: Restart a crashed service and immediately verify its live status.
 ↳ Command/Tool: systemctl restart my-app && systemctl status my-app
 Use Case: When a stuck background process needs a quick reboot to recover.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep runbook commands pre-tested so you can copy-paste them when half-asleep.
 ↳ Avoid writing vague steps like "investigate database" without exact commands.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SRE #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-28/morning/sre-runbooks-document-everything-so-3-am-doesnt-hurt-cheatsheet.pdf

---

*PDF: [sre-runbooks-document-everything-so-3-am-doesnt-hurt-cheatsheet.pdf](sre-runbooks-document-everything-so-3-am-doesnt-hurt-cheatsheet.pdf)*
