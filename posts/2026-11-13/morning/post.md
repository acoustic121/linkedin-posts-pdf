# Morning Post -- 2026-11-13

**Topic:** Cloud & DevOps Tips

---

Running a Kubernetes cluster without monitoring is like driving at night with your headlights off.
(with real examples you can use right now)

1. Enable Container Insights
 ↳ What: A built-in Azure add-on that collects performance metrics and logs from your cluster automatically.
 ↳ Command/Tool: az aks enable-addons -a monitoring -n myAKSCluster -g myResourceGroup
 Use Case: When launching a brand-new cluster and you need immediate visual health dashboards.

2. View Live Pod Logs
 ↳ What: A browser-based streaming view in the Azure Portal to see stdout/stderr logs in real time.
 ↳ Command/Tool: Azure Portal -> AKS -> Workloads -> Pods -> Live Data (Logs)
 Use Case: When an application crashes immediately on deploy and you need to see why right away.

3. Hunt Down High-Memory Pods
 ↳ What: A quick KQL database query to spot which container is eating all your cluster RAM.
 ↳ Command/Tool: KubePodInventory | summarize count() by ContainerStatus, PodName
 Use Case: When your cluster node runs out of memory and your boss asks which app caused it.

4. Detect Restarting Containers
 ↳ What: A query to find pods stuck in a CrashLoopBackOff loop before customers notice an outage.
 ↳ Command/Tool: KubePodInventory | where RestartCount > 3 | project PodName, Namespace, RestartCount
 Use Case: When users complain that the login service drops intermittently every 10 minutes.

5. Check Real-Time Node Utilization
 ↳ What: A lightweight CLI command to inspect current CPU and memory consumption across worker nodes.
 ↳ Command/Tool: kubectl top nodes
 Use Case: When a performance alert fires and you have 30 seconds to identify the overloaded node.

6. Setup a CPU Spike Alert
 ↳ What: An automated notification that triggers when cluster CPU usage stays above safe thresholds.
 ↳ Command/Tool: az monitor metrics alert create -n "HighCPUAlert" -g myRG --scopes <cluster-id> --condition "avg node_cpu_usage_percentage > 85"
 Use Case: When you want to sleep peacefully knowing Azure will wake you only if things catch fire.

7. Connect Managed Prometheus & Grafana
 ↳ What: A fully managed monitoring stack that provides industry-standard dashboards with zero maintenance.
 ↳ Command/Tool: az aks update -g myRG -n myAKSCluster --enable-azure-monitor-metrics
 Use Case: When your development team demands open-source Grafana boards without having to manage databases.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by mastering 3 basic KQL queries; Log Analytics is much easier once you understand filtering.
 ↳ Avoid logging full debug messages in production because Log Analytics ingestion costs will surprise you.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips


Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-13/morning/aks-monitoring-with-azure-monitor-container-insights-cheatsheet.pdf

---

*PDF: [aks-monitoring-with-azure-monitor-container-insights-cheatsheet.pdf](aks-monitoring-with-azure-monitor-container-insights-cheatsheet.pdf)*
