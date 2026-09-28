# Morning Post -- 2026-09-28

**Topic:** Cloud & DevOps Tips

---

Managing 20 different YAML files for a single Kubernetes app gets messy fast.
(with real examples you can use right now)

1. Creating a Starter Chart
 ↳ What: Generates a ready-to-use template folder with standard Kubernetes files.
 ↳ Command/Tool: helm create my-app
 Use Case: When you are starting a new microservice and need a clean Kubernetes boilerplate.

2. Installing an Application
 ↳ What: Deploys your packaged app into the Kubernetes cluster as a trackable release.
 ↳ Command/Tool: helm install my-release ./my-app
 Use Case: When you want to spin up your entire application stack on a cluster in one command.

3. Overriding Config on the Fly
 ↳ What: Changes default settings without editing any template files directly.
 ↳ Command/Tool: helm install my-release ./my-app --set replicaCount=3
 Use Case: When you need 3 pods in production but only 1 pod on your local test machine.

4. Inspecting Running Releases
 ↳ What: Lists every application deployed with Helm along with revision numbers and status.
 ↳ Command/Tool: helm list -A
 Use Case: When your team lead asks which version of the backend service is currently active.

5. Upgrading with Zero Downtime
 ↳ What: Applies new container images or config changes safely to your running app.
 ↳ Command/Tool: helm upgrade my-release ./my-app --set image.tag=v2.0.0
 Use Case: When you need to deploy a newly tested feature without kicking active users off the platform.

6. Instant Rollback for Broken Releases
 ↳ What: Reverts your app back to a previous healthy revision in seconds.
 ↳ Command/Tool: helm rollback my-release 1
 Use Case: When a new release causes 500 errors at 3 AM and you need to restore the working version fast.

7. Validating YAML Before Deployment
 ↳ What: Generates raw Kubernetes manifests locally to catch syntax bugs before touching the cluster.
 ↳ Command/Tool: helm template my-release ./my-app --debug
 Use Case: When you want to verify your YAML indentation and logic before opening a Pull Request.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep all environment-specific settings in separate values files (e.g., values-prod.yaml, values-dev.yaml).
 ↳ Never hardcode passwords or secrets directly inside your Chart templates or values files.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-28/morning/helm-charts-explained-package-kubernetes-apps-the-right-way-cheatsheet.pdf

---

*PDF: [helm-charts-explained-package-kubernetes-apps-the-right-way-cheatsheet.pdf](helm-charts-explained-package-kubernetes-apps-the-right-way-cheatsheet.pdf)*
