# Morning Post -- 2026-08-02

**Topic:** Cloud & DevOps Tips

---

Every DevOps engineer remembers their first day staring at a blank black Linux terminal...
(with real examples you can use right now)

1. Checking Server Space
 ↳ What: Tells you how much hard drive space is left on your server before things crash.
 ↳ Command/Tool: df -h
 Use Case: When your app suddenly stops saving files because the server is completely full at 3 AM.

2. Real-Time Log Watching
 ↳ What: Shows you the newest error messages popping up in your application files as they happen.
 ↳ Command/Tool: tail -f app.log
 Use Case: When your boss asks what went wrong and you need to watch the error happen live.

3. Finding Processes
 ↳ What: Helps you search for running programs so you can stop them when they freeze.
 ↳ Command/Tool: ps aux | grep python
 Use Case: When an old Python script is stuck running in the background and refusing to close.

4. Killing Stuck Apps
 ↳ What: Forcefully stops a misbehaving program that is eating up all your server memory.
 ↳ Command/Tool: kill -9 1234
 Use Case: When your web server freezes and normal shutdown buttons just won't work.

5. Checking File Permissions
 ↳ What: Shows who is allowed to read, write, or run a specific file or folder.
 ↳ Command/Tool: ls -l
 Use Case: When your script says 'Permission denied' and you need to see who owns the file.

6. Viewing Network Traffic
 ↳ What: Checks which ports and network connections are currently active on your machine.
 ↳ Command/Tool: netstat -tuln
 Use Case: When you want to check if your newly launched web app is actually listening on port 8080.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Practice these commands in a free cloud sandbox for 10 minutes every day.
 ↳ Never blindly copy-paste commands from random blogs without understanding them first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Linux #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-02/morning/linux-commands-every-devops-beginner-must-know-cheatsheet.pdf

---

*PDF: [linux-commands-every-devops-beginner-must-know-cheatsheet.pdf](linux-commands-every-devops-beginner-must-know-cheatsheet.pdf)*
