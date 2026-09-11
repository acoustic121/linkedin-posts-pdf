# Morning Post -- 2026-09-11

**Topic:** Cloud & DevOps Tips

---

Managing 100 servers manually feels like serving 100 people the exact same coffee one by one...
(with real examples you can use right now)

1. Check Server Specs (Grains)
 ↳ What: Grains are static details like OS, memory, and IP automatically collected from your servers.
 ↳ Command/Tool: salt '*' grains.item osfullname
 Use Case: When your manager asks which servers are still running outdated Linux versions.

2. Target Servers by OS (Grains Targeting)
 ↳ What: Filter and execute commands on specific server groups without remembering IP addresses.
 ↳ Command/Tool: salt -G 'os:Ubuntu' test.ping
 Use Case: When you need to restart web services only on Ubuntu servers during midnight maintenance.

3. Add Custom Server Tags (Custom Grains)
 ↳ What: Custom grains let you assign your own key-value labels to organize your fleet.
 ↳ Command/Tool: salt '*' grains.setval environment production
 Use Case: When you want to tag newly provisioned servers as 'staging' or 'production'.

4. Pass Secrets Safely (Pillars)
 ↳ What: Pillars store private data like passwords and API keys centrally and share them only with target servers.
 ↳ Command/Tool: salt '*' pillar.items
 Use Case: When you need to share secret database credentials with backend apps without hardcoding them.

5. View Specific Secrets (Pillar Query)
 ↳ What: Read specific configuration parameters assigned privately to an individual server node.
 ↳ Command/Tool: salt 'db-node-01' pillar.item db_password
 Use Case: When troubleshooting connection issues to see if a node received updated database keys.

6. Sync Updated Secrets (Refresh Pillar)
 ↳ What: Forces minion servers to fetch updated pillar values immediately from the master server.
 ↳ Command/Tool: salt '*' saltutil.refresh_pillar
 Use Case: When you rotate API keys on the master node and need all servers updated in seconds.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Think of Grains as a server's public resume and Pillars as its private vault.
 ↳ Never store passwords in Grains because Grain data is readable by all connected nodes.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SaltStack #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-11/morning/saltstack-pillars-grains-manage-server-config-at-scale-cheatsheet.pdf

---

*PDF: [saltstack-pillars-grains-manage-server-config-at-scale-cheatsheet.pdf](saltstack-pillars-grains-manage-server-config-at-scale-cheatsheet.pdf)*
