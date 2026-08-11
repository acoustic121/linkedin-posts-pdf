# Morning Post -- 2026-08-11

**Topic:** Cloud & DevOps Tips

---

Every junior engineer panics when an app crashes and someone says "check the logs"...
(with real examples you can use right now)

1. Watch Live Logs in Real Time
 ↳ What: See new log entries automatically stream on your screen as they happen.
 ↳ Command/Tool: tail -f /var/log/syslog
 Use Case: When your app crashes at 3am and you need to watch what happens during a retry.

2. Search for Specific Errors
 ↳ What: Filter through thousands of log lines to pinpoint exact error keywords.
 ↳ Command/Tool: grep -i "error" /var/log/nginx/error.log
 Use Case: When your boss asks why the web server is returning 500 status codes.

3. Read Modern System Service Logs
 ↳ What: View central system logs managed by modern Linux services.
 ↳ Command/Tool: journalctl -u nginx.service -n 50
 Use Case: When your database service refuses to start after a server reboot.

4. Inspect File Ends Quickly
 ↳ What: Read the last few lines of a log file without opening huge text files.
 ↳ Command/Tool: tail -n 20 /var/log/auth.log
 Use Case: When you want to see who recently attempted to log into your server via SSH.

5. Scroll Through Logs Safely
 ↳ What: Navigate large log files page-by-page without freezing your terminal memory.
 ↳ Command/Tool: less /var/log/syslog
 Use Case: When you need to read historical log entries from hours ago at your own pace.

6. Stream and Filter Simultaneously
 ↳ What: Watch live logs while hiding everything except critical failure messages.
 ↳ Command/Tool: tail -f /var/log/app.log | grep -i "failed"
 Use Case: When a noisy application generates millions of lines but you only care about failures.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with tail -f and grep first—80% of log debugging relies on just these two commands.
 ↳ Never run cat on multi-gigabyte log files or your terminal will freeze up.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Linux #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-11/morning/how-to-read-linux-logs-and-debug-issues-cheatsheet.pdf

---

*PDF: [how-to-read-linux-logs-and-debug-issues-cheatsheet.pdf](how-to-read-linux-logs-and-debug-issues-cheatsheet.pdf)*
