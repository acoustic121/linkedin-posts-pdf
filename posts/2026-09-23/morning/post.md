# Morning Post -- 2026-09-23

**Topic:** Cloud & DevOps Tips

---

Nothing hurts more than seeing 'OOMKilled' crash your app at 3 AM.
(with real examples you can use right now)

1. Memory Requests (The Reservation)
 ↳ What: The minimum amount of RAM your container is guaranteed to receive.
 ↳ Command/Tool: resources.requests.memory: "256Mi" in Pod YAML
 Use Case: When you want to guarantee your app gets scheduled only on a node that actually has room for it.

2. Memory Limits (The Hard Ceiling)
 ↳ What: The absolute maximum RAM your container can use before Kubernetes terminates it.
 ↳ Command/Tool: resources.limits.memory: "512Mi" in Pod YAML
 Use Case: When a memory leak tries to eat all the server RAM and threaten other apps on the same node.

3. Spotting OOMKilled Errors
 ↳ What: Finding out if Kubernetes killed your container because it exceeded its memory limit.
 ↳ Command/Tool: kubectl describe pod <pod-name> | grep -E "OOMKilled|Exit Code"
 Use Case: When your pod keeps restarting randomly and you need to confirm if it hit Exit Code 137.

4. Real-Time Resource Inspection
 ↳ What: A live snapshot showing which containers are eating the most RAM right now.
 ↳ Command/Tool: kubectl top pod --sort-by=memory
 Use Case: When your team notices high latency and needs to find the memory-hungry service in 5 seconds.

5. CPU Throttling Protection
 ↳ What: Giving your app CPU shares without putting a hard limit that slows it down.
 ↳ Command/Tool: resources.requests.cpu: "250m" (no cpu limit specified)
 Use Case: When your API responds slowly during traffic spikes because Kubernetes is throttling its CPU cycles.

6. Inspecting Dead Pod Logs
 ↳ What: Reading the final log lines written by a pod just before it was killed.
 ↳ Command/Tool: kubectl logs <pod-name> --previous
 Use Case: When your app crashes at night and normal logs only show the newly restarted container.

7. Checking Node Headroom
 ↳ What: Seeing how much total CPU and memory capacity is left across your servers.
 ↳ Command/Tool: kubectl top nodes
 Use Case: When your new deployment is stuck in 'Pending' status because no node has enough free resources.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set memory requests equal to memory limits for predictable Java or Node.js apps.
 ↳ Avoid setting strict CPU limits unless necessary, as CPU throttling causes sudden latency spikes.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-23/morning/kubernetes-resource-requests-limits-stop-getting-oomkilled-cheatsheet.pdf

---

*PDF: [kubernetes-resource-requests-limits-stop-getting-oomkilled-cheatsheet.pdf](kubernetes-resource-requests-limits-stop-getting-oomkilled-cheatsheet.pdf)*
