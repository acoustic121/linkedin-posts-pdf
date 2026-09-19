# Morning Post -- 2026-09-19

**Topic:** Cloud & DevOps Tips

---

Every Kubernetes beginner struggles with where to put their database passwords and API keys.
(with real examples you can use right now)

1. ConfigMap from Literal Values
 ↳ What: A way to store non-secret configuration data like application colors or API URLs as simple key-value pairs.
 ↳ Command/Tool: kubectl create configmap app-config --from-literal=APP_COLOR=blue
 Use Case: When your boss asks you to change the UI background color without rebuilding the entire Docker image.

2. ConfigMap from a File
 ↳ What: A way to load an entire configuration file directly into Kubernetes without typing it out manually.
 ↳ Command/Tool: kubectl create configmap app-settings --from-file=app.conf
 Use Case: When your app crashes at 3am because it needs a new database configuration file loaded immediately.

3. Generic Secret for Passwords
 ↳ What: A secure way to store sensitive information like passwords, tokens, or keys in your cluster.
 ↳ Command/Tool: kubectl create secret generic db-pass --from-literal=password=SuperSecret123
 Use Case: When you need to pass a database password to your backend pod without putting it in plain text on GitHub.

4. View ConfigMap Data
 ↳ What: A quick command to check the key-value pairs stored inside your ConfigMap to verify they are correct.
 ↳ Command/Tool: kubectl get configmap app-config -o yaml
 Use Case: When your app isn't connecting to the database and you need to check if the port number was set correctly.

5. Decode a Secret
 ↳ What: A command to safely decode and view the hidden base64 values of your Kubernetes Secret.
 ↳ Command/Tool: kubectl get secret db-pass -o jsonpath="{.data.password}" | base64 --decode
 Use Case: When a senior developer asks you to double-check if the database password was saved without typos.

6. Mount ConfigMap as a Volume
 ↳ What: A method to inject your configuration settings as actual files inside your running container.
 ↳ Command/Tool: kubectl set volume deployment/my-app --add --name=config-vol --mount-path=/config --configmap-name=app-settings
 Use Case: When your web server needs to read a custom configuration file directly from a specific folder.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always use ConfigMaps for public settings and Secrets for private ones—never mix them up.
 ↳ Avoid pushing base64 encoded Secrets to public git repositories thinking they are actually encrypted.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Kubernetes #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-09-19/morning/kubernetes-configmaps-secrets-manage-app-config-safely-cheatsheet.pdf

---

*PDF: [kubernetes-configmaps-secrets-manage-app-config-safely-cheatsheet.pdf](kubernetes-configmaps-secrets-manage-app-config-safely-cheatsheet.pdf)*
