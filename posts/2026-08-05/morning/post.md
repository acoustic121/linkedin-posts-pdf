# Morning Post -- 2026-08-05

**Topic:** Cloud & DevOps Tips

---

Every beginner stares at Kubernetes YAML files and wonders what actually runs inside them.
(with real examples you can use right now)

1. Pod
 ↳ What: The smallest running unit in Kubernetes that holds your app container.
 ↳ Command/Tool: kubectl run my-app --image=nginx
 Use Case: When you need to quickly test if your container image actually boots up without errors.

2. Deployment
 ↳ What: A smart manager that automatically keeps your app running and handles updates.
 ↳ Command/Tool: kubectl create deployment web --image=nginx --replicas=3
 Use Case: When your boss asks you to ensure the website stays up even if a server crashes.

3. Service
 ↳ What: A permanent network address that lets traffic find your changing pods.
 ↳ Command/Tool: kubectl expose deployment web --port=80 --type=NodePort
 Use Case: When you need to let users actually visit your app from outside the cluster.

4. Namespace
 ↳ What: Virtual walls inside your cluster that separate dev, test, and production apps.
 ↳ Command/Tool: kubectl create namespace staging
 Use Case: When you want to stop testing code from accidentally breaking the live production app.

5. ConfigMap
 ↳ What: A safe place to store non-secret settings like database URLs and feature flags.
 ↳ Command/Tool: kubectl create configmap app-config --from-literal=theme=dark
 Use Case: When you need to change how your app looks without rebuilding the whole Docker image.

6. Log Checker
 ↳ What: A built-in window to watch what your app is shouting about in real-time.
 ↳ Command/Tool: kubectl logs deployment/web
 Use Case: When the app crashes at 3 AM and you need to see the exact error message immediately.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with minikube or kind to run a local cluster on your laptop.
 ↳ Don't memorize YAML files; use kubectl dry-run commands to generate them.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-05/morning/kubernetes-in-plain-english-pods-services-deployments-cheatsheet.pdf

---

*PDF: [kubernetes-in-plain-english-pods-services-deployments-cheatsheet.pdf](kubernetes-in-plain-english-pods-services-deployments-cheatsheet.pdf)*
