# Morning Post -- 2026-09-03

**Topic:** Cloud & DevOps Tips

---

Every developer gets stuck debugging network traffic until they learn these 6 essential ports...
(with real examples you can use right now)

1. Web Traffic (Ports 80 & 443)
 ↳ What: The standard ports used for unencrypted HTTP and encrypted HTTPS web traffic.
 ↳ Command/Tool: curl -I https://google.com
 Use Case: When your frontend API request fails and you need to check if the server is responding.

2. Remote Server Access (Port 22)
 ↳ What: Secure Shell (SSH) port used to log into and manage remote servers safely.
 ↳ Command/Tool: ssh user@your-server-ip
 Use Case: When your senior dev asks you to jump into a Linux server and check the app logs.

3. Domain Name System (Port 53)
 ↳ What: The internet directory system that translates names like google.com into IP addresses.
 ↳ Command/Tool: nslookup google.com
 Use Case: When your app cannot connect to a remote service because domain resolution is broken.

4. Database Connections (Ports 5432 & 3306)
 ↳ What: The default ports for PostgreSQL (5432) and MySQL (3306) database services.
 ↳ Command/Tool: nc -zv backend-db.internal 5432
 Use Case: When your app crashes at startup with a target machine actively refused connection error.

5. Local Development (Ports 3000 & 8080)
 ↳ What: Common alternate web ports used for running applications locally on your laptop.
 ↳ Command/Tool: lsof -i :3000
 Use Case: When you run npm start and terminal screams port 3000 is already in use.

6. Redis Cache (Port 6379)
 ↳ What: The default network port for Redis, an in-memory database used for fast caching.
 ↳ Command/Tool: redis-cli -h 127.0.0.1 -p 6379 ping
 Use Case: When user login sessions suddenly drop because your cache layer went offline.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Test network connectivity with curl or nc before spending hours changing application code.
 ↳ Never leave database or SSH ports completely open to the internet in production.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Networking #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-03/morning/ports-protocols-what-every-developer-should-know-cheatsheet.pdf

---

*PDF: [ports-protocols-what-every-developer-should-know-cheatsheet.pdf](ports-protocols-what-every-developer-should-know-cheatsheet.pdf)*
