# Morning Post -- 2026-11-12

**Topic:** Cloud & DevOps Tips

---

Every DevOps engineer has seen pods stuck in 'Pending' state because the cluster ran out of memory...
(with real examples you can use right now)

1. Enable Autoscaler on a New Cluster
 ↳ What: Creates an AKS cluster that automatically adds or removes nodes as traffic changes.
 ↳ Command/Tool: az aks create --resource-group myRG --name myAKS --node-count 1 --enable-cluster-autoscaler --min-count 1 --max-count 5
 Use Case: When setting up a brand-new project that needs to handle sudden user spikes safely.

2. Turn On Autoscaler for Existing Pool
 ↳ What: Enables automatic node scaling on a cluster node pool you already created.
 ↳ Command/Tool: az aks update --resource-group myRG --name myAKS --enable-cluster-autoscaler --min-count 2 --max-count 10
 Use Case: When your manager tells you the app crashed at 3 AM because it ran out of server capacity.

3. Adjust Min and Max Node Limits
 ↳ What: Changes the safe boundaries of how small or large your cluster can scale.
 ↳ Command/Tool: az aks update --resource-group myRG --name myAKS --update-cluster-autoscaler --min-count 3 --max-count 15
 Use Case: When preparing your cluster for a big holiday sale and you need higher base capacity.

4. Inspect Autoscaler Status
 ↳ What: Displays real-time details about why nodes are being added or scaled down.
 ↳ Command/Tool: kubectl get configmap cluster-autoscaler-status -n kube-system -o yaml
 Use Case: When a developer asks why their new pod is waiting for a node to spin up.

5. Watch Nodes Scale in Real-Time
 ↳ What: Streams live status updates of cluster nodes as new virtual machines join.
 ↳ Command/Tool: kubectl get nodes -w
 Use Case: When testing autoscaling under load and you want to see new servers pop up live.

6. Disable Autoscaler Safely
 ↳ What: Turns off auto-scaling and locks the cluster to a fixed number of nodes.
 ↳ Command/Tool: az aks update --resource-group myRG --name myAKS --disable-cluster-autoscaler
 Use Case: When running fixed performance benchmarks and you don't want node counts changing.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with conservative max-count limits so you don't get a surprising cloud bill.
 ↳ Don't confuse Horizontal Pod Autoscaler (adds pods) with Cluster Autoscaler (adds nodes).

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AKS #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-12/morning/aks-cluster-autoscaler-scale-nodes-up-down-automatically-cheatsheet.pdf

---

*PDF: [aks-cluster-autoscaler-scale-nodes-up-down-automatically-cheatsheet.pdf](aks-cluster-autoscaler-scale-nodes-up-down-automatically-cheatsheet.pdf)*
