# Morning Post -- 2026-09-10

**Topic:** Cloud & DevOps Tips

---

Managing 100 servers manually feels like trying to cook dinner for 100 people with 1 microwave.
(with real examples you can use right now)

1. Salt Ping
 ↳ What: Checks if your central controller (Master) can talk to all servers (Minions).
 ↳ Command/Tool: salt '*' test.ping
 Use Case: When your lead asks if all server agents are online after a network maintenance window.

2. Remote Execution
 ↳ What: Runs a shell command on multiple servers at the exact same time.
 ↳ Command/Tool: salt '*' cmd.run 'uptime'
 Use Case: When your app slows down at 3am and you need to check server load instantly.

3. Salt States
 ↳ What: Defines what software should be installed and running automatically on your machines.
 ↳ Command/Tool: salt '*' state.apply nginx
 Use Case: When you need to install and configure Nginx across 10 web servers with one click.

4. Salt Grains
 ↳ What: Collects static system information like OS version, CPU, and memory specs.
 ↳ Command/Tool: salt '*' grains.item osfullname
 Use Case: When security asks you to list every server currently running an old Ubuntu version.

5. Salt Pillar
 ↳ What: Safely stores sensitive variables like passwords and API keys to send to specific servers.
 ↳ Command/Tool: salt 'db-prod*' pillar.items
 Use Case: When you need to pass database credentials safely without putting them in code files.

6. Target Filtering
 ↳ What: Directs commands to specific servers based on names or system properties.
 ↳ Command/Tool: salt -G 'os:Ubuntu' test.ping
 Use Case: When you want to push an update only to Ubuntu servers without touching CentOS machines.

7. Highstate Enforcement
 ↳ What: Syncs all your configuration rules at once to keep servers in their desired state.
 ↳ Command/Tool: salt '*' state.highstate
 Use Case: When someone manually changes a server config by mistake and you need to fix it fast.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by running safe read-only commands like test.ping on local virtual machines first.
 ↳ Avoid hardcoding passwords inside State YAML files; always use Pillars for secret data.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SaltStack #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-10/morning/saltstack-in-plain-english-configuration-management-made-easy-cheatsheet.pdf

---

*PDF: [saltstack-in-plain-english-configuration-management-made-easy-cheatsheet.pdf](saltstack-in-plain-english-configuration-management-made-easy-cheatsheet.pdf)*
