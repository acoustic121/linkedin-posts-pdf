# Morning Post -- 2026-11-24

**Topic:** Cloud & DevOps Tips

---

Every cloud engineer has woken up to a surprise $5,000 Azure bill...
(with real examples you can use right now)

1. Deny Expensive VM Sizes
 ↳ What: Prevents your team from launching high-cost virtual machines by mistake.
 ↳ Command/Tool: az policy definition create
 Use Case: When your team is testing and you don't want a $1,000/month VM spun up by accident.

2. Enforce Mandatory Tags
 ↳ What: Requires every resource to have a cost-center tag so you know who pays for it.
 ↳ Command/Tool: az policy assignment create
 Use Case: When your boss asks which team is responsible for a mysterious new database.

3. Restrict Resource Regions
 ↳ What: Blocks resource deployments outside of your approved geographical areas.
 ↳ Command/Tool: az policy assignment create --policy "Allowed locations"
 Use Case: When your data must stay in a specific country to comply with local privacy laws.

4. Run a Compliance Scan
 ↳ What: Scans your subscription to find resources that are breaking your active policies.
 ↳ Command/Tool: az policy state trigger-scan
 Use Case: When you inherit a messy Azure account and want a list of what needs fixing.

5. Remediate Broken Resources
 ↳ What: Automatically fixes non-compliant resources without you having to manually update each one.
 ↳ Command/Tool: az policy remediation create
 Use Case: When you need to quickly add missing security settings across fifty storage accounts.

6. Deploy Environments with Blueprints
 ↳ What: Package resource groups, policies, and permissions together to spin up a pre-configured sandbox.
 ↳ Command/Tool: Azure Portal -> Blueprints
 Use Case: When a new developer joins and you need to set up their workspace in five minutes.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with "Audit" mode first to see what's broken before you switch to "Deny" and block your developers.
 ↳ Don't enforce policies on the root management group unless you are absolutely sure of the impact.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-24/morning/azure-policy-blueprints-enforce-governance-across-your-subscriptions-cheatsheet.pdf

---

*PDF: [azure-policy-blueprints-enforce-governance-across-your-subscriptions-cheatsheet.pdf](azure-policy-blueprints-enforce-governance-across-your-subscriptions-cheatsheet.pdf)*
