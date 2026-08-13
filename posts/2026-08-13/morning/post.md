# Morning Post -- 2026-08-13

**Topic:** Cloud & DevOps Tips

---

Every Kubernetes beginner struggles with kubectl until they master these 7 commands...
(with real examples you can use right now)

1. Check What's Running
 ↳ What: Lists all active application pods in your current workspace.
 ↳ Command/Tool: kubectl get pods
 Use Case: When your manager asks if the new app version is deployed yet.

2. Read App Output Logs
 ↳ What: Displays the real-time output and error messages printed by your container.
 ↳ Command/Tool: kubectl logs -f <pod-name>
 Use Case: When the app crashes at 3am and you need to see what went wrong.

3. Inspect Pod Details
 ↳ What: Shows deep configuration details, health status, and recent cluster events.
 ↳ Command/Tool: kubectl describe pod <pod-name>
 Use Case: When your pod is stuck in 'CrashLoopBackOff' and won't start up.

4. Jump Inside a Container
 ↳ What: Opens an interactive terminal shell inside a running container.
 ↳ Command/Tool: kubectl exec -it <pod-name> -- /bin/bash
 Use Case: When you need to test database connectivity directly from the application.

5. Quick Port Forwarding
 ↳ What: Connects a local port on your laptop directly to a pod in the cluster.
 ↳ Command/Tool: kubectl port-forward pod/<pod-name> 8080:80
 Use Case: When you want to test a web app locally before exposing it to users.

6. Deploy App Configurations
 ↳ What: Creates or updates cluster resources using a configuration file.
 ↳ Command/Tool: kubectl apply -f deployment.yaml
 Use Case: When you need to push a new feature or setting change to the cluster.

7. Restart a Frozen App
 ↳ What: Performs a smooth restart of all containers managed by a deployment.
 ↳ Command/Tool: kubectl rollout restart deployment <deployment-name>
 Use Case: When an app gets unresponsive and a simple restart fixes the issue.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Set up a terminal alias like 'k' for 'kubectl' to save hours of typing.
 ↳ Avoid editing running cluster objects directly—always keep your YAML files in Git.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-13/morning/kubectl-commands-every-kubernetes-beginner-needs-cheatsheet.pdf

---

*PDF: [kubectl-commands-every-kubernetes-beginner-needs-cheatsheet.pdf](kubectl-commands-every-kubernetes-beginner-needs-cheatsheet.pdf)*
