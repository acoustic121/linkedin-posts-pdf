# Morning Post -- 2026-09-25

**Topic:** Cloud & DevOps Tips

---

Every developer eventually gets hit with a 'Permission Denied' error in Kubernetes...
(with real examples you can use right now)

1. Role (Namespace-Level Rules)
 ↳ What: Sets permissions like viewing or editing resources within a single namespace.
 ↳ Command/Tool: kubectl create role pod-reader --verb=get,list,watch --resource=pods -n dev
 Use Case: When a junior developer only needs to read pod logs inside the dev namespace.

2. ClusterRole (Cluster-Wide Rules)
 ↳ What: Sets permissions across the entire cluster, like viewing server nodes or persistent storage.
 ↳ Command/Tool: kubectl create clusterrole node-reader --verb=get,list --resource=nodes
 Use Case: When your monitoring app needs to collect health metrics from every node in the cluster.

3. RoleBinding (Linking User to Role)
 ↳ What: Attaches a Role to a user or service account inside one specific namespace.
 ↳ Command/Tool: kubectl create rolebinding read-pods --role=pod-reader --user=alex -n dev
 Use Case: When your lead asks you to give a new teammate access to inspect dev pods.

4. ClusterRoleBinding (Linking User Cluster-Wide)
 ↳ What: Attaches a ClusterRole to a user across every single namespace in your cluster.
 ↳ Command/Tool: kubectl create clusterrolebinding read-nodes --clusterrole=node-reader --user=alex
 Use Case: When an engineer needs access to troubleshoot cluster-wide infrastructure during an outage.

5. ServiceAccount (Bot Accounts for Apps)
 ↳ What: An identity created for applications and scripts to interact with the Kubernetes API safely.
 ↳ Command/Tool: `kubectl create serviceaccount deployment-bot -n dev`
 Use Case: When your CI/CD pipeline needs permission to automatically deploy app updates.

6. Permission Check (kubectl auth can-i)
 ↳ What: A quick check command to test if a specific user or bot can perform an action.
 ↳ Command/Tool: kubectl auth can-i delete pods --as=alex -n dev
 Use Case: When an app deployment fails with a 403 error and you need to test access rights.

7. User Impersonation (Test As Someone Else)
 ↳ What: Run commands as another user to test their permissions without taking their laptop.
 ↳ Command/Tool: kubectl get pods --as=alex -n dev
 Use Case: When a teammate says "I can't see the pods!" and you need to verify their view.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always grant minimum permissions needed (Principle of Least Privilege).
 ↳ Avoid giving normal users 'cluster-admin' privileges just to make things work.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-25/morning/kubernetes-rbac-who-can-do-what-in-your-cluster-cheatsheet.pdf

---

*PDF: [kubernetes-rbac-who-can-do-what-in-your-cluster-cheatsheet.pdf](kubernetes-rbac-who-can-do-what-in-your-cluster-cheatsheet.pdf)*
