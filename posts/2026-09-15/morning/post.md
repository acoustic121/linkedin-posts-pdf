# Morning Post -- 2026-09-15

**Topic:** Cloud & DevOps Tips

---

Imagine configuring 50 servers manually, one by one, installing the same packages—it's a recipe for typos.
(with real examples you can use right now)

1. The Master & Minion Relationship
 ↳ What: The central controller (Master) talking to the servers you manage (Minions).
 ↳ Command/Tool: salt '*' test.ping
 Use Case: When your manager asks if all 20 web servers are online and responding right now.

2. Installing Packages (The State File)
 ↳ What: A simple YAML file that describes what software should be installed on your servers.
 ↳ Command/Tool: pkg.installed
 Use Case: When you need to install Nginx on 10 new servers without SSHing into each one.

3. Managing Services (Keep it Running)
 ↳ What: Ensuring your installed software is actually running and starts automatically when the server boots.
 ↳ Command/Tool: service.running
 Use Case: When your website goes down because someone forgot to start the database service after a reboot.

4. Deploying Configuration Files
 ↳ What: Copying a local configuration file from your master server to all your minion servers automatically.
 ↳ Command/Tool: file.managed
 Use Case: When you need to update the website's index.html file across all production servers instantly.

5. Running a State File
 ↳ What: Telling SaltStack to read your configuration files and make the servers match that exact setup.
 ↳ Command/Tool: salt '*' state.apply webserver
 Use Case: When you've written your setup plan and want to configure all servers in one single click.

6. Gathering Server Info (Grains)
 ↳ What: Salt's built-in tool to collect static information like OS, IP address, and memory from your servers.
 ↳ Command/Tool: salt '*' grains.item osfullname
 Use Case: When you need to quickly find out which of your servers are running Ubuntu vs CentOS.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start small by managing a single local virtual machine before targeting production servers.
 ↳ Avoid writing hardcoded IP addresses; use Salt's built-in variables (Grains) instead.

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SaltStack #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-15/morning/saltstack-states-automate-server-setup-step-by-step-cheatsheet.pdf

---

*PDF: [saltstack-states-automate-server-setup-step-by-step-cheatsheet.pdf](saltstack-states-automate-server-setup-step-by-step-cheatsheet.pdf)*
