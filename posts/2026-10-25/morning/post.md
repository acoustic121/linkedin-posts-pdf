# Morning Post -- 2026-10-25

**Topic:** Cloud & DevOps Tips

---

The worst way to find out your production app is down is from an angry customer email.
(with real examples you can use right now)

1. Azure Metrics Explorer
 ↳ What: A built-in dashboard tool that charts performance numbers like CPU and memory in real time.
 ↳ Command/Tool: az monitor metrics list --resource <resource-id> --metric "Percentage CPU"
 Use Case: When your app feels sluggish and you want to see if the server is running out of CPU.

2. Log Analytics (KQL)
 ↳ What: A central place where all your app logs live, searchable with a simple query language called KQL.
 ↳ Command/Tool: az monitor log-analytics query -w <workspace-id> --analytics-query "AppExceptions | take 10"
 Use Case: When an API endpoint starts crashing and you need the exact error stack trace right away.

3. Metric Alert Rules
 ↳ What: An automatic tripwire that triggers a warning whenever a performance number crosses a danger threshold.
 ↳ Command/Tool: az monitor metrics alert create -n "HighCPUAlert" -g MyRG --scopes <vm-id> --condition "avg Percentage CPU > 85"
 Use Case: When you want to get notified automatically before your virtual machine freezes completely.

4. Action Groups
 ↳ What: A saved list of destinations—like your team's email, phone, or Slack—that receive alert notifications.
 ↳ Command/Tool: az monitor action-group create -g MyRG -n "DevOpsTeam" --email-receiver name="OnCall" email="oncall@company.com"
 Use Case: When a database goes down at 2 AM and the right engineer needs an immediate email.

5. Azure Activity Log
 ↳ What: A flight data recorder that tracks every administrative change made to your Azure resources.
 ↳ Command/Tool: az monitor activity-log list --max-events 10 --select eventTimestamp,caller,operationName
 Use Case: When a server unexpectedly stops and you need to find out who turned it off.

6. Application Insights
 ↳ What: An application performance monitoring tool that auto-detects slow API requests and broken dependencies.
 ↳ Command/Tool: az monitor app-insights component show -g MyRG -a "prod-app-insights"
 Use Case: When users report checkout delays and you need to know which database call is taking 10 seconds.

7. Service Health Alerts
 ↳ What: A free monitoring feed that informs you if Microsoft's own cloud hardware or region is having an outage.
 ↳ Command/Tool: az monitor activity-log alert create -g MyRG -n "OutageAlert" --condition category=ServiceHealth
 Use Case: When your cluster drops offline and you need to confirm whether it is your fault or an Azure datacenter outage.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start small by setting up one metric alert on CPU usage before building complex multi-service dashboards.

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-25/morning/azure-monitor-alerts-know-when-something-breaks-before-users-do-cheatsheet.pdf

---

*PDF: [azure-monitor-alerts-know-when-something-breaks-before-users-do-cheatsheet.pdf](azure-monitor-alerts-know-when-something-breaks-before-users-do-cheatsheet.pdf)*
