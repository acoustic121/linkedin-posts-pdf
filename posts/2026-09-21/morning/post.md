# Morning Post -- 2026-09-21

**Topic:** Cloud & DevOps Tips

---

Most beginners get confused by how external traffic actually reaches a Kubernetes pod.
(with real examples you can use right now)

1. The Traffic Cop (Ingress Controller)
 ↳ What: The actual software (like NGINX) that sits at the entrance of your cluster and routes incoming requests.
 ↳ Command/Tool: minikube addons enable ingress
 Use Case: When you need to set up the main entry point for all your web apps in your local lab.

2. Path-Based Routing
 ↳ What: Sending users to different services based on the URL path they type (like /api or /login).
 ↳ Command/Tool: kubectl create ingress path-ingress --rule="example.com/api*=api-service:80" --dry-run=client -o yaml
 Use Case: When your boss asks you to route all "/api" traffic to the backend and "/" to the frontend.

3. Domain-Based Routing
 ↳ What: Routing traffic to different services based on the domain name used (like app.com vs api.com).
 ↳ Command/Tool: kubectl create ingress domain-ingress --rule="app.example.com/*=app-service:80" --dry-run=client -o yaml
 Use Case: When your marketing team launches a new subdomain like "blog.company.com" and needs it hooked up to the blog service.

4. Secure Traffic (SSL/TLS)
 ↳ What: Adding an SSL certificate to your Ingress so your website uses secure HTTPS instead of HTTP.
 ↳ Command/Tool: kubectl create secret tls cert-secret --cert=path/to/tls.crt --key=path/to/tls.key
 Use Case: When your security team says "no HTTP allowed" and you need to secure your app in 5 minutes.

5. The Status Check
 ↳ What: Finding out the public IP address assigned to your Ingress so you can map your domain to it.
 ↳ Command/Tool: kubectl get ingress
 Use Case: When your app isn't loading and you need to check if the Ingress actually got a public IP.

6. Troubleshooting Logs
 ↳ What: Looking inside the Ingress controller to see why a request is failing with a 404 or 502 error.
 ↳ Command/Tool: kubectl logs -n ingress-nginx -l app.kubernetes.io/name=ingress-nginx --tail=10
 Use Case: When a user complains about a "502 Bad Gateway" at 3 AM and you need to find the broken backend service.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with path-based routing on localhost using Minikube before trying complex domains.
 ↳ Never forget to create the target Service first, or your Ingress will route traffic to nowhere.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-21/morning/kubernetes-ingress-route-traffic-to-the-right-service-cheatsheet.pdf

---

*PDF: [kubernetes-ingress-route-traffic-to-the-right-service-cheatsheet.pdf](kubernetes-ingress-route-traffic-to-the-right-service-cheatsheet.pdf)*
