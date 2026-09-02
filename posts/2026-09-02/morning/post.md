# Morning Post -- 2026-09-02

**Topic:** Cloud & DevOps Tips

---

Every developer has watched their app crash when unexpected traffic hits.
(with real examples you can use right now)

1. Metrics Server
 ↳ What: Collects live CPU and memory usage data from all your running pods.
 ↳ Command/Tool: kubectl top pods
 Use Case: When your app feels slow and you need to spot the resource hog fast.

2. Resource Requests
 ↳ What: Sets the baseline CPU and memory your app needs so HPA can calculate percentages.
 ↳ Command/Tool: kubectl set resources deployment my-app --requests=cpu=200m
 Use Case: When you need to guarantee your app gets enough resources to even start up.

3. Auto-Create HPA
 ↳ What: Tells Kubernetes to automatically add pods when CPU usage goes over your target percentage.
 ↳ Command/Tool: kubectl autoscale deployment my-app --min=2 --max=10 --cpu-percent=80
 Use Case: When your boss asks how the app will handle 5x more users tonight.

4. HPA Status Check
 ↳ What: Gives you a quick overview of current usage versus your scaling targets.
 ↳ Command/Tool: kubectl get hpa my-app
 Use Case: When you want to double-check if your autoscaler is actually active.

5. Scaling Event Logs
 ↳ What: Shows the exact history of why and when Kubernetes added or removed pods.
 ↳ Command/Tool: kubectl describe hpa my-app
 Use Case: When the app scaled up at 3 AM and you need to investigate why.

6. Real-Time Pod Watch
 ↳ What: Streams pod creations and terminations live on your screen as autoscaling happens.
 ↳ Command/Tool: kubectl get pods -w
 Use Case: When you generate test load and want to watch extra pods spawn in real time.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set resource requests on your deployments, or HPA won't know when to scale!
 ↳ Don't set your max replicas too high initially, or a runaway process could drain your cloud budget.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-02/morning/how-kubernetes-scales-your-app-automatically-hpa-cheatsheet.pdf

---

*PDF: [how-kubernetes-scales-your-app-automatically-hpa-cheatsheet.pdf](how-kubernetes-scales-your-app-automatically-hpa-cheatsheet.pdf)*
