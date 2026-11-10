# Morning Post -- 2026-11-10

**Topic:** Cloud & DevOps Tips

---

Giving a developer full cluster access just to check logs is like giving your house keys to a guest to use the bathroom.
(with real examples you can use right now)

1. Entra ID Integrated Cluster Creation
 ↳ What: Connects your Azure logins directly to your Kubernetes cluster so you don't manage separate user passwords.
 ↳ Command/Tool: az aks create --resource-group myRG --name myAKS --enable-azure-rbac
 Use Case: When setting up a new cluster and you want your team to log in using their normal work email.

2. Grant Basic Cluster Access
 ↳ What: Gives a team member permission to sign into the cluster without making them an admin.
 ↳ Command/Tool: az role assignment create --assignee dev@company.com --role "Azure Kubernetes Service Cluster User Role" --scope /subscriptions/SUB_ID/resourceGroups/myRG/providers/Microsoft.ContainerService/managedClusters/myAKS
 Use Case: When a new developer joins your team and needs basic kubectl access.

3. Fetch Safe Login Credentials
 ↳ What: Downloads a safe login file so your local command line can talk to the cluster using your Azure account.
 ↳ Command/Tool: az aks get-credentials --resource-group myRG --name myAKS
 Use Case: When you need to connect your laptop terminal to the company Kubernetes cluster for the first time.

4. Read-Only Access to a Namespace
 ↳ What: Restricts a user so they can only view resources inside a single project space.
 ↳ Command/Tool: kubectl create rolebinding dev-view --clusterrole=view --user=dev@company.com --namespace=app-dev
 Use Case: When an intern needs to inspect running pods in the dev environment without breaking anything.

5. Admin Access for Emergency Ops
 ↳ What: Gives full administrative control over the cluster only to trusted senior operations engineers.
 ↳ Command/Tool: az role assignment create --assignee admin@company.com --role "Azure Kubernetes Service Cluster Admin Role" --scope /subscriptions/SUB_ID/resourceGroups/myRG/providers/Microsoft.ContainerService/managedClusters/myAKS
 Use Case: When your senior SRE needs full control to fix a critical networking issue during a outage.

6. Verify Your Own Access Rights
 ↳ What: Checks if your account has permission to perform a specific action before you try it.
 ↳ Command/Tool: kubectl auth can-i delete pods --namespace app-dev
 Use Case: When you want to check if you have permission to delete a stuck pod before running the command.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always grant access at the namespace level first instead of giving cluster-wide rights.
 ↳ Avoid sharing static admin kubeconfig files over Slack or email.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips


Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-10/morning/aks-rbac-azure-ad-integration-secure-who-can-touch-your-cluster-cheatsheet.pdf

---

*PDF: [aks-rbac-azure-ad-integration-secure-who-can-touch-your-cluster-cheatsheet.pdf](aks-rbac-azure-ad-integration-secure-who-can-touch-your-cluster-cheatsheet.pdf)*
