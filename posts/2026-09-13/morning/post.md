# Morning Post -- 2026-09-13

**Topic:** Cloud & DevOps Tips

---

Imagine logging into 100 servers one by one just to update a single security patch...
(with real examples you can use right now)

1. Ping All Servers at Once
 ↳ What: Send a quick heartbeat check to every connected server to verify connectivity.
 ↳ Command/Tool: salt '*' test.ping
 Use Case: When your manager asks if all web servers survived a sudden network outage.

2. Target Servers by OS
 ↳ What: Filter and run commands only on servers running a specific operating system.
 ↳ Command/Tool: salt -G 'os:Ubuntu' test.ping
 Use Case: When you need to update Ubuntu machines without touching your RedHat database servers.

3. Check Disk Space Globally
 ↳ What: Gather disk usage details across your entire infrastructure in seconds.
 ↳ Command/Tool: salt '*' disk.usage
 Use Case: When an alert fires at 3am saying a log folder filled up somewhere in the cluster.

4. Execute Raw Terminal Commands
 ↳ What: Run standard Linux shell commands on all targeted servers simultaneously.
 ↳ Command/Tool: salt '*' cmd.run 'uptime'
 Use Case: When you need to know which servers have been running the longest without a reboot.

5. Bulk Package Installation
 ↳ What: Install or update software packages across all servers with one execution.
 ↳ Command/Tool: salt '*' pkg.install nginx
 Use Case: When you need to deploy Nginx across 50 new worker nodes before a product launch.

6. Apply Configuration States
 ↳ What: Enforce defined system settings so every server matches your exact setup rules.
 ↳ Command/Tool: salt '*' state.apply webserver
 Use Case: When someone manually broke a config file and you need to restore the correct version everywhere.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always test your server target filters with test.ping before running destructive commands.
 ↳ Avoid using cmd.run for permanent changes; use Salt states so your setup stays repeatable.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SaltStack #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-13/morning/how-saltstack-runs-commands-across-100-servers-at-once-cheatsheet.pdf

---

*PDF: [how-saltstack-runs-commands-across-100-servers-at-once-cheatsheet.pdf](how-saltstack-runs-commands-across-100-servers-at-once-cheatsheet.pdf)*
