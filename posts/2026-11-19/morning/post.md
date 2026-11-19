# Morning Post -- 2026-11-19

**Topic:** Cloud & DevOps Tips

---

Imagine a power outage wipes out an entire data center, but your app stays online...
(with real examples you can use right now)

1. Checking Zone Support in a Region
 ↳ What: A quick way to check which Azure regions offer isolated data centers called Availability Zones.
 ↳ Command/Tool: az account list-locations --query "[?metadata.regionType=='Physical'].{Name:name, Zones:availabilityZoneMappings}" -o table
 Use Case: When your manager asks which nearby cloud region can survive a major disaster.

2. Zone-Redundant Storage (ZRS)
 ↳ What: Automatically keeps 3 copies of your files stored across 3 separate physical data centers.
 ↳ Command/Tool: az storage account create --name mystorage123 --resource-group myRG --location eastus --sku Standard_ZRS
 Use Case: When user uploaded photos must stay safe even if an entire data center floods.

3. Pinning Virtual Machines to a Zone
 ↳ What: Creating a virtual machine inside one specific data center for ultimate control.
 ↳ Command/Tool: az vm create --resource-group myRG --name myVM1 --image Ubuntu2204 --zone 1 --generate-ssh-keys
 Use Case: When you want your database primary in Zone 1 and your backup server in Zone 2.

4. Zone-Redundant Public IP
 ↳ What: A resilient IP address that routes internet traffic even if two data centers go dark.
 ↳ Command/Tool: az network public-ip create --resource-group myRG --name myPublicIP --sku Standard --zone 1 2 3
 Use Case: When your application needs a static entry point that never drops during a cloud outage.

5. Verifying VM Size Availability
 ↳ What: Checking if a specific virtual machine size is actually available in your target zone.
 ↳ Command/Tool: az vm list-skus --location eastus --size Standard_B2s --query "[].{Size:name, Zones:locationInfo[0].zones}" -o table
 Use Case: When Azure gives you a frustrating error saying a server size is not available in Zone 1.

6. High-Availability Web Apps
 ↳ What: Hosting your web code across multiple data centers without managing underlying servers.
 ↳ Command/Tool: az appservice plan create --name myAppPlan --resource-group myRG --number-of-workers 3 --zone-redundant
 Use Case: When your client demands a bulletproof web app without paying for a full DevOps team.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Always choose Standard SKU resources because Basic SKUs do not support Availability Zones.
 ↳ Avoid putting all your virtual machines into a single zone when trying to build high availability.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-19/morning/azure-availability-zones-build-apps-that-survive-a-data-centre-failure-cheatsheet.pdf

---

*PDF: [azure-availability-zones-build-apps-that-survive-a-data-centre-failure-cheatsheet.pdf](azure-availability-zones-build-apps-that-survive-a-data-centre-failure-cheatsheet.pdf)*
