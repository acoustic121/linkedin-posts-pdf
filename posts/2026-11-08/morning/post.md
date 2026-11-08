# Morning Post -- 2026-11-08

**Topic:** Cloud & DevOps Tips

---

Managing Kubernetes master nodes used to take hours until Azure started doing it for us.
(with real examples you can use right now)

1. Creating an AKS Cluster
 ↳ What: Azure sets up and manages the control plane for free so you only pay for worker nodes.
 ↳ Command/Tool: az aks create --resource-group myRG --name myAKSCluster --node-count 2 --generate-ssh-keys
 Use Case: When your team needs a Kubernetes environment fast without building servers from scratch.

2. Connecting kubectl to AKS
 ↳ What: Downloads cluster access credentials so your local terminal can control your Azure cluster.
 ↳ Command/Tool: az aks get-credentials --resource-group myRG --name myAKSCluster
 Use Case: When your manager gives you cluster access and asks you to deploy an app today.

3. Scaling Worker Nodes
 ↳ What: Increases or decreases the number of worker servers in your cluster on demand.
 ↳ Command/Tool: az aks scale --resource-group myRG --name myAKSCluster --node-count 4
 Use Case: When you expect high traffic during a flash sale and need extra server power.

4. Enabling Cluster Autoscaler
 ↳ What: Automatically adds worker servers when your pods run out of CPU or memory space.
 ↳ Command/Tool: az aks update --resource-group myRG --name myAKSCluster --enable-cluster-autoscaler --min-count 1 --max-count 5
 Use Case: When your app crashes at 3am because unexpected traffic overwhelmed your nodes.

5. Checking Cluster Node Health
 ↳ What: Shows the status of all worker nodes to verify if servers are healthy and ready.
 ↳ Command/Tool: kubectl get nodes -o wide
 Use Case: When a deployment fails and you need to see if a worker server went offline.

6. Upgrading Kubernetes Version
 ↳ What: Updates your cluster version safely while keeping your application running continuously.
 ↳ Command/Tool: az aks upgrade --resource-group myRG --name myAKSCluster --kubernetes-version 1.28.3
 Use Case: When your security team requires you to patch old software without breaking production.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with a 1-node cluster in test environments to keep your cloud bill near zero.
 ↳ Don't forget to delete your resource group when you finish testing for the day.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AKS #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-08/morning/aks-explained-run-kubernetes-on-azure-without-managing-masters-cheatsheet.pdf

---

*PDF: [aks-explained-run-kubernetes-on-azure-without-managing-masters-cheatsheet.pdf](aks-explained-run-kubernetes-on-azure-without-managing-masters-cheatsheet.pdf)*
