# Morning Post -- 2026-08-22

**Topic:** Cloud & DevOps Tips

---

Every DevOps engineer relies on these 6 Grafana tools when the app crashes at 3 AM...
(with real examples you can use right now)

1. Local Grafana Setup
 ↳ What: Spin up a complete Grafana dashboard server on your machine in seconds.
 ↳ Command/Tool: docker run -d -p 3000:3000 --name=grafana grafana/grafana
 Use Case: When you want to practice creating dashboards on your laptop without touching production.

2. PromQL CPU Query
 ↳ What: A metric query language used in Grafana to calculate system resource usage.
 ↳ Command/Tool: 100 - (avg by(instance)(rate(node_cpu_seconds_total{mode="idle"}[5m])) * 100)
 Use Case: When your manager asks why the application server is suddenly running so slow.

3. LogQL Error Filtering
 ↳ What: A query tool powered by Grafana Loki to search live log stream text.
 ↳ Command/Tool: {app="payment-service"} |= "error"
 Use Case: When an API fails at 3 AM and you need to find the exact error log immediately.

4. Dashboard Importing
 ↳ What: A quick feature to load pre-built community dashboards using a unique ID.
 ↳ Command/Tool: Grafana Import Dashboard -> ID: 1860
 Use Case: When you need a full Linux server monitoring dashboard setup in under 2 minutes.

5. Admin Password Reset
 ↳ What: A command-line tool to reset dashboard credentials when locked out.
 ↳ Command/Tool: grafana-cli admin reset-admin-password newpass123
 Use Case: When you forget your local Grafana login password during an urgent debugging session.

6. Grafana Unified Alerting
 ↳ What: An automated trigger system that sends alerts to Slack or Email when metrics spike.
 ↳ Command/Tool: Grafana Alert Rules -> Contact Point: Slack Webhook
 Use Case: When memory hits 90% so you get notified before the app completely crashes.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Import community dashboards first instead of building complex panels from scratch.
 ↳ Never query raw logs across 30 days without filters or your browser will crash.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Grafana #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-22/morning/what-is-grafana-dashboards-that-save-you-at-3-am-cheatsheet.pdf

---

*PDF: [what-is-grafana-dashboards-that-save-you-at-3-am-cheatsheet.pdf](what-is-grafana-dashboards-that-save-you-at-3-am-cheatsheet.pdf)*
