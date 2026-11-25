# Morning Post -- 2026-11-25

**Topic:** Cloud & DevOps Tips

---

Every time Microsoft updates your cloud server, your app usually goes offline.
(with real examples you can use right now)

1. Availability Set
 ↳ What: A logical grouping of virtual machines that tells Azure to keep your servers on separate physical hardware.
 ↳ Command/Tool: Azure Portal -> Create a resource -> Availability set
 Use Case: When your boss asks you to stop the app from crashing during routine server maintenance.

2. Fault Domains
 ↳ What: Racks in the data center that share the same power source and network switch.
 ↳ Command/Tool: `az vm availability-set show --resource-group MyRG --name MyAvailabilitySet`
 Use Case: When a power supply blows up in a server rack, your second server keeps the website running.

3. Update Domains
 ↳ What: Groups of virtual machines that get rebooted at the same time during backend Azure updates.
 ↳ Command/Tool: `az vm list-availability-set-updatedomains --resource-group MyRG --name MyAvailabilitySet`
 Use Case: When Microsoft patches a security hole, only half your servers restart so users don't notice a thing.

4. Managed Disks
 ↳ What: Virtual hard drives that Azure manages automatically so they don't break when hardware fails.
 ↳ Command/Tool: Azure Portal -> Disks -> Create managed disk
 Use Case: When you need to attach storage to your VMs that won't get lost if a physical hard drive dies.

5. Load Balancer
 ↳ What: A traffic cop that sends user requests to whichever server is currently awake and working.
 ↳ Command/Tool: Azure Portal -> Create a resource -> Load balancer
 Use Case: When traffic spikes and you need to spread users evenly across your protected servers.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always set up your availability sets *before* you deploy your virtual machines.
 ↳ Don't put all your app servers in a single update domain or they will all reboot together.

- - - 

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-25/morning/azure-availability-sets-protect-vms-from-planned-unplanned-downtime-cheatsheet.pdf

---

*PDF: [azure-availability-sets-protect-vms-from-planned-unplanned-downtime-cheatsheet.pdf](azure-availability-sets-protect-vms-from-planned-unplanned-downtime-cheatsheet.pdf)*
