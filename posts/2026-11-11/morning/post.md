# Morning Post -- 2026-11-11

**Topic:** Cloud & DevOps Tips

---

Every beginner creates 5 Load Balancers before discovering Kubernetes Ingress...
(with real examples you can use right now)

1. Add the NGINX Helm Repository
 ↳ What: Download the catalog that contains the official NGINX Ingress installation files.
 ↳ Command/Tool: helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx && helm repo update
 Use Case: When your team needs standard community tools installed on a brand-new AKS cluster.

2. Install the NGINX Controller
 ↳ What: Spin up a smart reverse proxy pod and an Azure Public Load Balancer with one command.
 ↳ Command/Tool: helm install my-ingress ingress-nginx/ingress-nginx --create-namespace --namespace ingress-basic
 Use Case: When your manager asks to put a single front-door router in front of 10 microservices.

3. Grab the Azure Public IP
 ↳ What: Find the single external IP address that Azure assigned to your ingress controller.
 ↳ Command/Tool: kubectl get service -n ingress-basic my-ingress-ingress-nginx-controller
 Use Case: When your DNS admin asks for the A-record IP to point your company domain name.

4. Deploy an Internal Service (ClusterIP)
 ↳ What: Run your web app pod and make it reachable only inside the Kubernetes network.
 ↳ Command/Tool: kubectl create deployment web-demo --image=nginx && kubectl expose deployment web-demo --port=80
 Use Case: When you want to keep backend pods safe from direct public internet exposure.

5. Create the Ingress Routing Rule
 ↳ What: Write a YAML traffic sign telling NGINX which URL path sends requests to which app.
 ↳ Command/Tool: kubectl apply -f ingress-rule.yaml (specifying rules.http.paths to backend services)
 Use Case: When you want user traffic for /api to hit the Node app and / to hit the frontend.

6. Test the Route Using cURL
 ↳ What: Send an HTTP request directly to your public IP to verify routing works before editing DNS.
 ↳ Command/Tool: curl -v http://<EXTERNAL-IP>/web-demo
 Use Case: When a developer complains their service is down at 2 PM and you need to pinpoint the routing bug.

7. Tail NGINX Traffic Logs
 ↳ What: Stream live incoming requests and status codes passing through the ingress controller.
 ↳ Command/Tool: kubectl logs -n ingress-basic -l app.kubernetes.io/name=ingress-nginx -f
 Use Case: When a user gets a 502 Bad Gateway and you need to see if NGINX can reach the backend pod.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set your backend Kubernetes services to type ClusterIP, never LoadBalancer, when using Ingress.
 ↳ Never forget to set ingressClassName: nginx in your Ingress manifest, or your rules will sit unapplied.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips


Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-11/morning/aks-ingress-with-nginx-route-external-traffic-to-your-services-cheatsheet.pdf

---

*PDF: [aks-ingress-with-nginx-route-external-traffic-to-your-services-cheatsheet.pdf](aks-ingress-with-nginx-route-external-traffic-to-your-services-cheatsheet.pdf)*
