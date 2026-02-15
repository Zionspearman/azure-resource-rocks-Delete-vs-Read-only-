# Azure Resource Locks Lab: Delete vs Read-only (RG vs Resource Scope)

This repository supports my lab walkthrough video on using **Azure Resource Locks** to protect resources by applying **Delete** and **Read-only** locks at different scopes and validating what actions are blocked.  
📺 **Watch the lab video on YouTube:** (add your link)

---

## 🔍 Lab Overview

In this lab, you’ll learn how to:

- Create and manage **resource locks** in Azure
- Apply **Delete** locks to prevent accidental deletion
- Apply **Read-only** locks to prevent updates and configuration changes
- Compare locks at **Resource Group** scope vs **Resource** scope
- Troubleshoot common “why can’t I delete/update?” scenarios

These tasks are fundamental for governance and protecting critical resources in production environments.

---

## 🧪 Lab Scenario

Your organization has critical resources that must be protected from accidental deletion or unauthorized changes. You are responsible for implementing governance controls using Azure resource locks to prevent destructive actions and enforce change control.

---

## 🛠️ Key Tasks

✅ **Task 1: Create the Lab Resource Group**
- Create a resource group named `rg-lock-lab`
- Deploy a low-cost resource (example: Storage account or Public IP)

✅ **Task 2: Apply a Delete Lock (Resource Group Scope)**
- Add a **Delete** lock named `lock-delete-rg` to `rg-lock-lab`
- Attempt to delete a resource (or the resource group) to confirm:
  - Deletion is blocked

✅ **Task 3: Apply a Read-only Lock (Resource Group Scope)**
- Replace the delete lock (or remove it) and add a **Read-only** lock named `lock-readonly-rg`
- Attempt to update a resource setting or tags to confirm:
  - Updates are blocked

✅ **Task 4: Apply Locks at Resource Scope (Optional)**
- Add **Delete** and/or **Read-only** locks directly on a single resource
- Validate that only that resource is restricted (when RG is not locked)

✅ **Task 5: Cleanup**
- Remove locks first
- Delete the resource group `rg-lock-lab`

---

## 📁 Suggested Files

- `lab-guide.md`: Full lab steps in markdown format for offline use  
- `screenshots/`: Visuals of locks, blocked actions, and error messages  
- `notes.md` (optional): Quick “exam takeaways” like lock behavior + scope differences  

---

## 🔗 Learn More

- [Lock your Azure resources to prevent accidental changes](https://learn.microsoft.com/azure/azure-resource-manager/management/lock-resources)  
- [Azure RBAC overview (related)](https://learn.microsoft.com/azure/role-based-access-control/overview)  
- [Understand RBAC scopes (related)](https://learn.microsoft.com/azure/role-based-access-control/scope-overview)

---

## 🧵 Tags

`#Azure` `#ResourceLocks` `#Governance` `#AZ104` `#AzureLabs` `#CloudSecurity`

Created by: **Zion Spearman**  
Use and modify this lab freely for study and practice.
