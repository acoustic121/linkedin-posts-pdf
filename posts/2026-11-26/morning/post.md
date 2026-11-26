# Morning Post -- 2026-11-26

**Topic:** Cloud & DevOps Tips

---

Every cloud beginner gets confused when choosing between Azure Blob and File storage...
(with real examples you can use right now)

1. Create a Storage Account
 ↳ What: The parent folder in Azure that holds all your cloud files, databases, and assets.
 ↳ Command/Tool: `az storage account create --name mystorageacct --resource-group myRG --location eastus --sku Standard_LRS`
 Use Case: When setting up your very first cloud workspace for your team's application.

2. Upload a profile picture (Blob Storage)
 ↳ What: Cheap, massive storage for unstructured files like images, videos, and PDFs.
 ↳ Command/Tool: `az storage blob upload --account-name mystorageacct --container-name images --name profile.jpg --file ./profile.jpg`
 Use Case: When your website's users need to upload and display their profile avatars.

3. Create a Shared Network Folder (Azure Files)
 ↳ What: A shared drive that multiple servers can connect to and read from at the same time.
 ↳ Command/Tool: `az storage share create --account-name mystorageacct --name appshares`
 Use Case: When you have three virtual machines that all need to access the same config folder.

4. Transfer massive folders super fast (AzCopy)
 ↳ What: A high-performance command-line tool designed for bulk copying data into and out of Azure.
 ↳ Command/Tool: `azcopy copy "C:\local\logs" "https://mystorageacct.blob.core.windows.net/logs?[SAS_TOKEN]"`
 Use Case: When your database backup finishes and you need to ship it to the cloud immediately.

5. Mount a shared folder locally
 ↳ What: Mapping your Azure File share directly to your laptop so it looks like a local drive.
 ↳ Command/Tool: `net use Z: \\mystorageacct.file.core.windows.net\appshares /user:Azure\mystorageacct [AccountKey]`
 Use Case: When your manager asks you to quickly edit files in the cloud using Notepad.

6. Check your storage usage
 ↳ What: Quick way to find out the total size of your storage files to monitor costs.
 ↳ Command/Tool: `az storage blob list --account-name mystorageacct --container-name images --query "[].{Name:name, Size:properties.contentLength}" --output table`
 Use Case: When the Finance team asks why the cloud bill went up this month.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Use Blob Storage for your app's code files/images, and File Storage for your servers' configurations.
 ↳ Avoid uploading sensitive files publicly without setting up Shared Access Signatures (SAS) first.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Azure #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-26/morning/azure-blob-vs-file-storage-which-one-to-use-and-when-cheatsheet.pdf

---

*PDF: [azure-blob-vs-file-storage-which-one-to-use-and-when-cheatsheet.pdf](azure-blob-vs-file-storage-which-one-to-use-and-when-cheatsheet.pdf)*
