# 🔐 Azure Identity and Governance

This project demonstrates how to manage users, roles, policies, and governance in Microsoft Azure.

## 🎯 Objectives

- Create and manage users and groups in **Microsoft Entra ID**
- Assign and interpret **RBAC roles**
- Apply and monitor **Azure Policies**
- Protect critical resources using **Resource Locks**
- Export role assignments via PowerShell

---

## 🧠 Key Concepts

| Feature | Description |
|----------|--------------|
| Microsoft Entra ID | Manages users, groups, and access permissions. |
| RBAC | Controls what users can do within Azure. |
| Azure Policy | Enforces organizational rules automatically. |
| Resource Locks | Prevents accidental deletion or modification. |

---

## ⚙️ Steps Implemented

1. **Created Users and Groups**
   - In Azure Portal → *Microsoft Entra ID → Users → New user*
   - Created users: `HR_Admin`, `Developer_A`, `Analyst_B`
   - Created groups: `Developers` and assigned members.

2. **Assigned Roles**
   - Navigated to *Subscription → Access Control (IAM)*  
   - Assigned roles:
     - `Owner` to Dejen Teklit  
     - `Reader` to Tibeb Dejen  
     - `VM Contributor` to Reai Dejen

3. **Applied Azure Policy**
   - Created a policy to restrict resource creation to “West Europe”.
   - Assigned it at the subscription level.

4. **Added Resource Locks**
   - Protected critical resources under *Resource Group → Locks → Add Lock*.

5. **Exported Role Assignments**
   ```powershell
   Get-AzRoleAssignment | Export-Csv "RoleAssignments.csv" -NoTypeInformation

