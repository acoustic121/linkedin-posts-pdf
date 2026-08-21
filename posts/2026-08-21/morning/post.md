# Morning Post -- 2026-08-21

**Topic:** Cloud & DevOps Tips

---

Every junior DevOps engineer dreads seeing the 'CrashLoopBackOff' status on a Monday morning...
(with real examples you can use right now)

1. Checking Pod Status
 ↳ What: Checking if your application containers are running, restarting, or failing.
 ↳ Command/Tool: kubectl get pods
 Use Case: When your manager asks why users are suddenly seeing error pages on the website.

2. Reading Past Logs
 ↳ What: Looking at the logs of the container right before it crashed and restarted.
 ↳ Command/Tool: kubectl logs <pod-name> --previous
 Use Case: When an app crashed 5 minutes ago and you need to find the exact error message.

3. Inspecting Pod Events
 ↳ What: Checking the system events to see why a container failed to start or run.
 ↳ Command/Tool: kubectl describe pod <pod-name>
 Use Case: When a pod is stuck in 'ContainerCreating' and you do not know why.

4. Detecting Memory Limits
 ↳ What: Finding out if the system killed your pod for using too much RAM.
 ↳ Command/Tool: kubectl get pod <pod-name> -o jsonpath='{.status.containerStatuses[*].lastState.terminated.reason}'
 Use Case: When your application works fine with 5 users but crashes during a load test.

5. Following Live Logs
 ↳ What: Watching logs print on your screen in real-time as they happen.
 ↳ Command/Tool: kubectl logs -f <pod-name>
 Use Case: When you are testing a new feature in staging and want to watch it run.

6. Verifying Server Health
 ↳ What: Checking if the underlying server running your pods is healthy and has resources.
 ↳ Command/Tool: kubectl get nodes
 Use Case: When multiple different applications crash at the exact same time.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always use the '--previous' flag when debugging restarted pods, otherwise you only see empty logs.
 ↳ Don't assume every crash is a code bug; check your configuration and environment variables first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-21/morning/what-happens-when-a-kubernetes-pod-crashes-cheatsheet.pdf

---

*PDF: [what-happens-when-a-kubernetes-pod-crashes-cheatsheet.pdf](what-happens-when-a-kubernetes-pod-crashes-cheatsheet.pdf)*
