# Morning Post -- 2026-10-24

**Topic:** Cloud & DevOps Tips

---

Every sysadmin has saved a VM snapshot right before running a risky update.
(with real examples you can use right now)

1. Creating a Quick Snapshot
 ↳ What: Saves the exact disk state of your VM before you make changes.
 ↳ Command/Tool: New-VMSnapshot -VM "AppServer" -Name "Pre-Patch" -Memory:$false
 Use Case: Right before you apply a major software patch at 2 AM.

2. Rolling Back to Safety
 ↳ What: An instant undo button that resets your VM to when the snapshot was taken.
 ↳ Command/Tool: Set-VM -VM "AppServer" -Snapshot "Pre-Patch" -Confirm:$false
 Use Case: When the patch crashes your app and your boss asks for an immediate fix.

3. Listing All Active Snapshots
 ↳ What: Finds all lingering snapshots so you can clean up hidden storage hogs.
 ↳ Command/Tool: Get-VM | Get-VMSnapshot | Select-Object VM, Name, Created, SizeGB
 Use Case: When the storage admin sends an alert that datastore space is at 95%.

4. Deleting & Merging Snapshots
 ↳ What: Merges changes safely into the main disk without losing your recent work.
 ↳ Command/Tool: Remove-VMSnapshot -Snapshot "Pre-Patch" -Confirm:$false
 Use Case: When your app upgrade succeeds and you no longer need the safety net.

5. Consolidating Stuck Disks
 ↳ What: Cleans up orphan snapshot files leftover after a backup job finishes.
 ↳ Command/Tool: (Get-VM "AppServer").ExtensionData.ConsolidateVMDisks()
 Use Case: When vCenter displays a yellow warning saying disk consolidation is required.

6. Checking Snapshots via ESXCLI
 ↳ What: Inspects snapshot details directly on the host when vCenter is slow.
 ↳ Command/Tool: vim-cmd vmsvc/snapshot.get [VM-ID]
 Use Case: When the vCenter Web UI is lagging during an active production issue.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Keep snapshots for less than 48 hours—they are safety nets, not backups.
 ↳ Avoid including RAM in snapshots unless necessary, as it freezes the VM longer.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #VMware #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-10-24/morning/vcenter-snapshots-save-restore-vms-the-right-way-cheatsheet.pdf

---

*PDF: [vcenter-snapshots-save-restore-vms-the-right-way-cheatsheet.pdf](vcenter-snapshots-save-restore-vms-the-right-way-cheatsheet.pdf)*
