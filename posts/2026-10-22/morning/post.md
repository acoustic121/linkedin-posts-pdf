# Morning Post -- 2026-10-22

**Topic:** Cloud & DevOps Tips

---

People think SREs just stare at complex dashboards all day, but here is what they actually do...
(with real examples you can use right now)

1. Service Health Checks
 ↳ What: Checking if your backend API is up and responding with a good status code.
 ↳ Command/Tool: curl -I -s https://httpbin.org/status/200
 Use Case: When your manager asks if the production API server is live right now.

2. Real-Time Log Triage
 ↳ What: Watching live application logs to catch errors the moment they happen.
 ↳ Command/Tool: tail -f /var/log/nginx/error.log | grep "ERROR"
 Use Case: When users report that clicking the payment button fails at 3am.

3. Server Resource Monitoring
 ↳ What: Checking how much CPU and memory your system is using to spot bottlenecks.
 ↳ Command/Tool: htop
 Use Case: When a server suddenly slows down and you need to find the process hogging CPU.

4. Network Connectivity Diagnostics
 ↳ What: Testing if your application server can reach the database on a specific port.
 ↳ Command/Tool: nc -zv db.internal.net 5432
 Use Case: When your app cannot connect to the database after a network update.

5. Alert Silencing
 ↳ What: Temporarily pausing noisy alerts during planned maintenance work.
 ↳ Command/Tool: amtool silence add alertname=HighCpuUsage --duration=1h
 Use Case: When performing server upgrades so you do not trigger false alarms for your team.

6. Container Health Verification
 ↳ What: Inspecting running containers to see if any microservices keep crashing.
 ↳ Command/Tool: kubectl get pods --field-selector=status.phase=Running
 Use Case: When verifying if all services successfully started after a new deployment.

7. Instant Application Rollback
 ↳ What: Reverting your deployed application back to the previous working version.
 ↳ Command/Tool: kubectl rollout undo deployment/web-app
 Use Case: When a new code update breaks the login page immediately after release.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by practicing basic log search commands on your local terminal.
 ↳ Never run manual troubleshooting commands on production without testing in staging first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #SRE #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-22/morning/sre-101-what-site-reliability-engineers-actually-do-all-day-cheatsheet.pdf

---

*PDF: [sre-101-what-site-reliability-engineers-actually-do-all-day-cheatsheet.pdf](sre-101-what-site-reliability-engineers-actually-do-all-day-cheatsheet.pdf)*
