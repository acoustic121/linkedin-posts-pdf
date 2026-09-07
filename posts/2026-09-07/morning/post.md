# Morning Post -- 2026-09-07

**Topic:** Cloud & DevOps Tips

---

People ask me what a Cloud Operations Engineer actually does all day.
(with real examples you can use right now)

1. Server Health Check
 ↳ What: Checking if your cloud server is running out of CPU or memory.
 ↳ Command/Tool: htop
 Use Case: When users report that your web app is suddenly running super slow.

2. Reading Live Logs
 ↳ What: Watching real-time error messages printed by your cloud application.
 ↳ Command/Tool: kubectl logs -f <pod-name>
 Use Case: When an app crashes in production and you need to see the stack trace instantly.

3. Disk Space Monitoring
 ↳ What: Checking how much storage space is left on your server hard drive.
 ↳ Command/Tool: df -h
 Use Case: When your database crashes at 3am because giant log files filled up the disk.

4. Network Connectivity Diagnostics
 ↳ What: Testing if your application server can talk to a database port.
 ↳ Command/Tool: nc -zv db.example.com 5432
 Use Case: When your backend app fails to connect to PostgreSQL after a new deployment.

5. Managing Containers
 ↳ What: Listing all active software containers running on your host machine.
 ↳ Command/Tool: docker ps
 Use Case: When your manager asks if all backend microservices are up and healthy.

6. Checking Open Network Ports
 ↳ What: Seeing which network ports your server is currently listening on.
 ↳ Command/Tool: ss -tuln
 Use Case: When you start a web server on port 8080 but get a Connection Refused error.

7. Cloud Resource Status
 ↳ What: Checking the operational status of virtual machines from your terminal.
 ↳ Command/Tool: aws ec2 describe-instances --output table
 Use Case: When you need to verify which cloud servers are running without opening a browser.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by practicing Linux commands on a free-tier virtual machine.
 ↳ Avoid memorizing flags; learn how to read terminal help documentation instead.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #CloudOperations #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-07/morning/what-does-a-cloud-operations-engineer-actually-do-cheatsheet.pdf

---

*PDF: [what-does-a-cloud-operations-engineer-actually-do-cheatsheet.pdf](what-does-a-cloud-operations-engineer-actually-do-cheatsheet.pdf)*
