# Morning Post -- 2026-11-09

**Topic:** Cloud & DevOps Tips

---

Most developers run all their Kubernetes apps on one giant VM size...
(with real examples you can use right now)

1. System Node Pool
 ↳ What: A dedicated group of VMs just for critical Kubernetes system services.
 ↳ Command/Tool: az aks nodepool add --resource-group MyRG --cluster-name MyAKS --name syspool --mode System --node-vm-size Standard_DS2_v2
 Use Case: When your web app crashes and you still need cluster management to stay alive.

2. User Node Pool
 ↳ What: A separate pool of VMs created specifically to run your main applications.
 ↳ Command/Tool: az aks nodepool add --resource-group MyRG --cluster-name MyAKS --name apppool --mode User --node-vm-size Standard_D2s_v5
 Use Case: When you want to run your APIs without disturbing cluster core operations.

3. Spot Node Pool
 ↳ What: Deeply discounted VMs using Azure's spare capacity for up to 90% savings.
 ↳ Command/Tool: az aks nodepool add --resource-group MyRG --cluster-name MyAKS --name spotpool --priority Spot --eviction-policy Delete --node-vm-size Standard_D2s_v5
 Use Case: When your boss asks you to run nightly data processing on a tight budget.

4. Memory-Optimized Pool
 ↳ What: High-RAM VMs designed for memory-heavy tools like Redis or databases.
 ↳ Command/Tool: az aks nodepool add --resource-group MyRG --cluster-name MyAKS --name mempool --node-vm-size Standard_E2s_v5
 Use Case: When your cache server keeps crashing with Out of Memory errors on standard VMs.

5. Node Selector Target
 ↳ What: A simple rule in your deployment YAML to send pods to a specific pool.
 ↳ Command/Tool: nodeSelector: agentpool: mempool
 Use Case: When you need to force your heavy cache container onto high-memory nodes.

6. Cluster Autoscaler
 ↳ What: Automatically adds or removes VMs in a pool based on real-time pod demand.
 ↳ Command/Tool: az aks nodepool update --resource-group MyRG --cluster-name MyAKS --name apppool --enable-cluster-autoscaler --min-count 1 --max-count 5
 Use Case: When traffic spikes at 9 AM and your team is still asleep.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with 2 pools: one low-cost System pool and one standard User pool for apps
 ↳ Never run production stateful databases on Spot node pools

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AKS #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-09/morning/aks-node-pools-mix-vm-sizes-for-cost-performance-cheatsheet.pdf

---

*PDF: [aks-node-pools-mix-vm-sizes-for-cost-performance-cheatsheet.pdf](aks-node-pools-mix-vm-sizes-for-cost-performance-cheatsheet.pdf)*
