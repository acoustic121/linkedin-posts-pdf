# Morning Post -- 2026-08-06

**Topic:** Cloud & DevOps Tips

---

Every time you type a website name into your browser, a tiny digital detective goes to work behind the scenes...
(with real examples you can use right now)

1. Browser Cache
 ↳ What: Your computer remembers websites you visited recently so it doesn't have to search again.
 ↳ Command/Tool: chrome://net-internals/#dns
 Use Case: When you want to check what website addresses your browser has saved locally.

2. Operating System Cache
 ↳ What: Your computer's main memory keeps a phone book of recent website addresses.
 ↳ Command/Tool: ipconfig /displaydns
 Use Case: When your boss asks you why the staging site is showing the old page.

3. The Internet Router
 ↳ What: Your home or office Wi-Fi box asks your internet provider for the website's real number.
 ↳ Command/Tool: nslookup google.com
 Use Case: When you need to find out what IP address a website is currently pointing to.

4. Root Name Servers
 ↳ What: The internet's global master directory that points traffic to the right ending like .com or .org.
 ↳ Command/Tool: dig +trace google.com
 Use Case: When the app crashes at 3am and you need to trace every single step of a DNS lookup.

5. Authoritative Name Server
 ↳ What: The final boss that holds the actual official address of the website you want.
 ↳ Command/Tool: dig google.com NS
 Use Case: When you are setting up a new domain name for your personal portfolio.

6. Flushing DNS
 ↳ What: Clearing out your computer's website phone book to force it to get fresh information.
 ↳ Command/Tool: ipconfig /flushdns
 Use Case: When a website is not loading for you, but works fine on everyone else's phone.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always check your local cache first before blaming the cloud servers
 ↳ Avoid changing your network DNS settings without knowing your default gateway

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Networking #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-08-06/morning/dns-explained-how-your-browser-finds-a-website-cheatsheet.pdf

---

*PDF: [dns-explained-how-your-browser-finds-a-website-cheatsheet.pdf](dns-explained-how-your-browser-finds-a-website-cheatsheet.pdf)*
