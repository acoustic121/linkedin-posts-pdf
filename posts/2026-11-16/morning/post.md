# Morning Post -- 2026-11-16

**Topic:** Cloud & DevOps Tips

---

Every developer starts building Kubernetes manually until they learn this simple Terraform trick.
(with real examples you can use right now)

1. Azure CLI Authentication
 ↳ What: Connects your local terminal to your Azure account so Terraform can work.
 ↳ Command/Tool: az login
 Use Case: When you need to let your terminal talk to your company Azure account.

2. AzureRM Provider Setup
 ↳ What: Tells Terraform to download the official Azure plugin so it understands Azure code.
 ↳ Command/Tool: provider "azurerm" { features {} }
 Use Case: Before writing any code, to load the tools Terraform needs to build Azure resources.

3. Resource Group Definition
 ↳ What: Creates a single folder in Azure to hold your cluster and network components.
 ↳ Command/Tool: resource "azurerm_resource_group" "rg"
 Use Case: When your lead asks you to organize project resources so they are easy to clean up.

4. Managed AKS Cluster Block
 ↳ What: Defines your actual Kubernetes cluster and its worker machines in a few lines of code.
 ↳ Command/Tool: resource "azurerm_kubernetes_cluster" "aks"
 Use Case: When you need a ready-to-use Kubernetes cluster without clicking 50 portal buttons.

5. Terraform Plan Preview
 ↳ What: Shows you a clear preview of everything Terraform is about to create before touching cloud.
 ↳ Command/Tool: terraform plan
 Use Case: When you want to double-check your code to avoid breaking existing production setups.

6. Terraform Apply Execution
 ↳ What: Builds your live AKS cluster in Azure automatically based on your code file.
 ↳ Command/Tool: terraform apply -auto-approve
 Use Case: When you are ready to provision your full Kubernetes infrastructure with one command.

7. Cluster Access Fetch
 ↳ What: Downloads access keys so your local kubectl tool can talk to the new cluster.
 ↳ Command/Tool: az aks get-credentials --resource-group myRG --name myAKS
 Use Case: When the cluster is ready and you want to deploy your first app container.

The best way to learn? Open a terminal and try these yourself.

My advice:
 ↳ Start with 1 small worker node (like Standard_B2s) so you do not get a surprise Azure bill.
 ↳ Never hardcode your Azure secret keys directly inside `.tf` code files.

- - -

Found this helpful? Follow me (Aman Raj Singh) for daily Cloud & DevOps tips

#CloudDevOps #DevOps #Terraform #Beginners #CloudNative

Download the full PDF cheatsheet:
https://github.com/acoustic121/linkedin-posts-pdf/raw/main/posts/2026-11-16/morning/provision-aks-with-terraform-full-infrastructure-as-code-example-cheatsheet.pdf

---

*PDF: [provision-aks-with-terraform-full-infrastructure-as-code-example-cheatsheet.pdf](provision-aks-with-terraform-full-infrastructure-as-code-example-cheatsheet.pdf)*
