# Morning Post -- 2026-11-17

**Topic:** Cloud & DevOps Tips

---

Every time you log into your office apps with one click, you are using Azure Entra ID.
(with real examples you can use right now)

1. Tenant
 ↳ What: Think of this as your organization's private digital apartment building inside Azure.
 ↳ Command/Tool: Azure Portal -> Microsoft Entra ID -> Overview
 Use Case: When your company needs a secure digital home for all employee accounts and apps.

2. User Account
 ↳ What: The digital ID card that proves who you are to the system.
 ↳ Command/Tool: New-AzADUser or Azure Portal (Users -> New user)
 Use Case: When a new teammate joins and needs their own login to access company tools.

3. Single Sign-On (SSO)
 ↳ What: The magic key that lets you log in once and open 10 different apps without re-typing your password.
 ↳ Command/Tool: Enterprise Applications -> New application -> Setup SSO
 Use Case: When your boss asks you to stop forcing people to remember five different passwords.

4. Multi-Factor Authentication (MFA)
 ↳ What: A second security check, like a text code or app tap, to prove you are really you.
 ↳ Command/Tool: Microsoft Entra ID -> Security -> Conditional Access
 Use Case: When you want to stop hackers even if they somehow steal your password.

5. Role-Based Access Control (RBAC)
 ↳ What: Giving people only the keys they need for their job, like giving IT staff room keys but keeping them out of accounting.
 ↳ Command/Tool: Access control (IAM) -> Add role assignment
 Use Case: When an intern joins and you need to let them view servers without letting them delete production.

6. Enterprise Application
 ↳ What: Any third-party app like Slack or GitHub connected to your company login system.
 ↳ Command/Tool: Microsoft Entra ID -> Enterprise applications
 Use Case: When your team wants to use a new SaaS tool using company login credentials.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always test access changes on a dummy test user before touching production accounts.
 ↳ Never give anyone Global Administrator rights unless they absolutely need full control.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-17/morning/azure-active-directory-entra-id-identity-sso-explained-simply-cheatsheet.pdf

---

*PDF: [azure-active-directory-entra-id-identity-sso-explained-simply-cheatsheet.pdf](azure-active-directory-entra-id-identity-sso-explained-simply-cheatsheet.pdf)*
