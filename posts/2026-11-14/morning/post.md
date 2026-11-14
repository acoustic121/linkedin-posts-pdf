# Morning Post -- 2026-11-14

**Topic:** Cloud & DevOps Tips

---

Every Kubernetes beginner panics when a Pod restarts and all its data disappears...
(with real examples you can use right now)

1. PersistentVolumeClaim (PVC)
 ↳ What: A request form your app submits to ask Kubernetes for permanent storage from Azure.
 ↳ Command/Tool: kubectl get pvc
 Use Case: When you need to request 10GB of dedicated disk space before launching your app.

2. Azure Disk (ReadWriteOnce)
 ↳ What: High-speed storage attached like a virtual hard drive to a single container.
 ↳ Command/Tool: kubectl get storageclass managed-csi
 Use Case: When your database pod needs fast private storage that no other pod touches.

3. Azure Files (ReadWriteMany)
 ↳ What: Shared cloud storage that multiple pods can read and write to at the same time.
 ↳ Command/Tool: kubectl get storageclass azurefile-csi
 Use Case: When you scale your web app to 5 pods and all of them need access to user uploads.

4. Dynamic Provisioning
 ↳ What: Automatic creation of Azure storage resources behind the scenes without using the Azure Portal.
 ↳ Command/Tool: kubectl get pv
 Use Case: When your boss asks you to deploy 10 new pods with dedicated disks in under two minutes.

5. Volume Mounts
 ↳ What: Attaching your requested Azure storage folder directly to a path inside your running container.
 ↳ Command/Tool: kubectl describe pod <pod-name>
 Use Case: When your app crashes at 3am and you need to confirm logs are writing to /mnt/azure.

6. Volume Snapshots
 ↳ What: A point-in-time backup copy of your Azure Disk storage to prevent accidental data loss.
 ↳ Command/Tool: kubectl get volumesnapshot
 Use Case: When you need to take a quick safety backup right before running a risky database patch.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with managed-csi storage class because Azure handles all the backend setup for you.
 ↳ Avoid using ReadWriteOnce disks when scaling app replicas across multiple nodes.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #AKS #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-14/morning/aks-persistent-storage-use-azure-disks-file-shares-in-pods-cheatsheet.pdf

---

*PDF: [aks-persistent-storage-use-azure-disks-file-shares-in-pods-cheatsheet.pdf](aks-persistent-storage-use-azure-disks-file-shares-in-pods-cheatsheet.pdf)*
