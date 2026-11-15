# Morning Post -- 2026-11-15

**Topic:** Cloud & DevOps Tips

---

Stop running kubectl apply manually every time you update your app...
(with real examples you can use right now)

1. Git as Single Source of Truth
 ↳ What: Storing all Kubernetes configuration files in Git so your cluster automatically matches your repository.
 ↳ Command/Tool: git commit -am "Update web deployment replicas to 3"
 Use Case: When your team lead asks who changed the cluster configuration and why.

2. AKS Cluster Connection
 ↳ What: Authenticating your local terminal with Azure Kubernetes Service so you can manage your cluster.
 ↳ Command/Tool: az aks get-credentials --resource-group myRG --name myAKSCluster
 Use Case: When setting up your developer machine to access the company Azure cluster for the first time.

3. Installing ArgoCD Operator
 ↳ What: Setting up ArgoCD inside your cluster so it can watch your Git repository for changes.
 ↳ Command/Tool: kubectl create namespace argocd && kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
 Use Case: When you want an automated agent inside your cluster deploying code for you.

4. Connecting Apps with ArgoCD
 ↳ What: Linking a Git folder containing YAML manifests directly to your AKS namespace.
 ↳ Command/Tool: argocd app create my-app --repo https://github.com/myorg/aks-apps.git --path app-yaml --dest-server https://kubernetes.default.svc --dest-namespace default
 Use Case: When you want your web app to deploy automatically every time you push to main.

5. Bootstrapping Flux v2
 ↳ What: An alternative lightweight GitOps tool that configures itself directly from your GitHub repository.
 ↳ Command/Tool: flux bootstrap github --owner=mygithubuser --repository=aks-fleet --path=clusters/production
 Use Case: When you prefer a hands-off tool running quiet syncs in the background without a UI.

6. Checking Deployment Sync Status
 ↳ What: Verifying whether your live cluster matches the code committed in your Git repository.
 ↳ Command/Tool: argocd app get my-app
 Use Case: When a developer asks why their newly pushed features are not live on the website yet.

7. Instant Rollbacks via Git
 ↳ What: Reverting a broken deployment by simply rolling back a commit in your Git history.
 ↳ Command/Tool: git revert HEAD && git push origin main
 Use Case: When the app crashes at 3am after a release and you need to restore the working version instantly.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start by practicing GitOps on a local Minikube or free Azure trial cluster before touching company infra.
 ↳ Avoid editing resources directly in the cluster using kubectl edit because GitOps will overwrite your changes.

- - -


Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-15/morning/gitops-on-aks-with-flux-or-argocd-deploy-from-git-automatically-cheatsheet.pdf

---

*PDF: [gitops-on-aks-with-flux-or-argocd-deploy-from-git-automatically-cheatsheet.pdf](gitops-on-aks-with-flux-or-argocd-deploy-from-git-automatically-cheatsheet.pdf)*
