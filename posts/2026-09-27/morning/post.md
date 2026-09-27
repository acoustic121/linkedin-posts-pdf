# Morning Post -- 2026-09-27

**Topic:** Cloud & DevOps Tips

---

Every junior developer starts with Kubernetes Deployments, but then their database crashes and they lose all their data.
(with real examples you can use right now)

1. Creating a StatefulSet
 ↳ What: A way to run database-like apps where each copy needs its own unique name and permanent storage.
 ↳ Command/Tool: kubectl apply -f statefulset.yaml
 Use Case: When your boss asks you to host a PostgreSQL database on Kubernetes without losing data.

2. Checking Pod Identity
 ↳ What: Watching how pods get stable, predictable names (like db-0, db-1) instead of random letters.
 ↳ Command/Tool: kubectl get pods -l app=postgres -w
 Use Case: When you need to know exactly which database pod is the primary one.

3. Headless Services
 ↳ What: A special service that lets database pods talk directly to each other by name rather than through a single IP.
 ↳ Command/Tool: kubectl get service postgres-headless
 Use Case: When your database replicas need to sync data directly with the main database.

4. Persistent Volume Claims (PVC)
 ↳ What: A request for dedicated hard drive space that stays attached to your pod even if it restarts.
 ↳ Command/Tool: kubectl get pvc
 Use Case: When your app crashes at 3am and you need to make sure the data is still there when it boots back up.

5. Scaling Up and Down
 ↳ What: Adding or removing database pods one by one in a strict, predictable order.
 ↳ Command/Tool: kubectl scale statefulset postgres --replicas=3
 Use Case: When traffic spikes on Black Friday and you need to safely add database replicas without breaking replication.

6. Deleting a StatefulSet Safely
 ↳ What: Removing the database pods while keeping your actual data disks completely safe and untouched.
 ↳ Command/Tool: kubectl delete statefulset postgres --cascade=orphan
 Use Case: When you want to upgrade your database setup without accidentally wiping out production customer data.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by deploying a simple Nginx StatefulSet before trying complex databases like MongoDB.
 ↳ Never manually delete PVCs unless you are 100% sure you do not need that data anymore.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-27/morning/kubernetes-statefulsets-when-deployments-arent-enough-cheatsheet.pdf

---

*PDF: [kubernetes-statefulsets-when-deployments-arent-enough-cheatsheet.pdf](kubernetes-statefulsets-when-deployments-arent-enough-cheatsheet.pdf)*
