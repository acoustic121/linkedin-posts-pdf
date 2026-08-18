# Morning Post -- 2026-08-18

**Topic:** Cloud & DevOps Tips

---

Every developer has stared at a "Permission Denied" error and blindly run "chmod 777"...
(with real examples you can use right now)

1. View File Permissions
 ↳ What: Checking who owns a file and what actions they are allowed to perform.
 ↳ Command/Tool: ls -l config.json
 Use Case: When your app fails to start and you need to see if the system can actually access its config file.

2. Make a Script Executable
 ↳ What: Giving a script file the permission to run as a program.
 ↳ Command/Tool: chmod +x deploy.sh
 Use Case: When you write a deployment bash script but get "Permission denied" when trying to run it.

3. Change File Owner
 ↳ What: Transferring ownership of a file to another user or group on the system.
 ↳ Command/Tool: sudo chown nginx:nginx app.log
 Use Case: When your web server throws a 500 error because it doesn't own its own log files.

4. Secure Private Keys
 ↳ What: Restricting a file so only the owner can read it, and nobody else can touch it.
 ↳ Command/Tool: chmod 400 my-key.pem
 Use Case: When SSH refuses to connect to your AWS server because your private key is "too open."

5. Change Folder and Subfolder Owners
 ↳ What: Changing the owner of a directory and every single file inside it all at once.
 ↳ Command/Tool: sudo chown -R ubuntu:ubuntu /var/www/html
 Use Case: When you copy a website folder to your server and need to make sure your user can edit everything inside.

6. Standard File Permissions
 ↳ What: Allowing the owner to read and write a file, while everyone else can only read it.
 ↳ Command/Tool: chmod 644 index.html
 Use Case: When you want your HTML files to be readable by the public web server, but only modifiable by you.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Use "chmod +x" instead of "chmod 777" when you just want to run a script.
 ↳ Never use "chmod 777" in production because it lets anyone read, write, and run your files.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Linux #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-18/morning/linux-file-permissions-explained-chmod-chown-cheatsheet.pdf

---

*PDF: [linux-file-permissions-explained-chmod-chown-cheatsheet.pdf](linux-file-permissions-explained-chmod-chown-cheatsheet.pdf)*
