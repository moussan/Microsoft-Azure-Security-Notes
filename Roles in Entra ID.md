# Understand Roles in Microsoft Entra ID

*Last updated: 07/30/2024*

There are about 60 Microsoft Entra built-in roles, which are roles with a fixed set of role permissions. To supplement the built-in roles, Microsoft Entra ID also supports custom roles. Use custom roles to select the role permissions that you want. For example, you could create one to manage particular Microsoft Entra resources such as applications or service principals.

This article explains what Microsoft Entra roles are and how they can be used.

---

## How Microsoft Entra Roles Differ from Other Microsoft 365 Roles

There are many different services in Microsoft 365, such as Microsoft Entra ID and Intune. Some of these services have their own role-based access control systems, specifically:

- Microsoft Entra ID
- Microsoft Exchange
- Microsoft Intune
- Microsoft Defender for Cloud Apps
- Microsoft 365 Defender portal
- Compliance portal
- Cost Management + Billing

Other services such as Teams, SharePoint, and Managed Desktop don’t have separate role-based access control systems. They use Microsoft Entra roles for their administrative access. Azure has its own role-based access control system for Azure resources such as virtual machines, and this system is not the same as Microsoft Entra roles.

**Azure RBAC versus Microsoft Entra roles:**  
When we say separate role-based access control system, it means there is a different data store where role definitions and role assignments are stored. Similarly, there is a different policy decision point where access checks happen.  
For more information, see *Roles across Microsoft services and Azure roles, Microsoft Entra roles, and classic subscription administrator roles*.

---

## Why Some Microsoft Entra Roles Are for Other Services

Microsoft 365 has a number of role-based access control systems that developed independently over time, each with its own service portal. To make it convenient for you to manage identity across Microsoft 365 from the Microsoft Entra admin center, we have added some service-specific built-in roles, each of which grants administrative access to a Microsoft 365 service.

For example, the **Exchange Administrator** role in Microsoft Entra ID is equivalent to the Organization Management role group in the Exchange role-based access control system, and can manage all aspects of Exchange. Similarly, we added the **Intune Administrator** role, **Teams Administrator**, **SharePoint Administrator**, and so on.

---

## Categories of Microsoft Entra Roles

Microsoft Entra built-in roles differ in where they can be used, which fall into the following three broad categories:

1. **Microsoft Entra ID-specific roles:**  
   These roles grant permissions to manage resources within Microsoft Entra-only.  
   *Examples: User Administrator, Application Administrator, Groups Administrator.*

2. **Service-specific roles in Microsoft Entra ID:**  
   Microsoft services such as Microsoft 365 define roles in Microsoft Entra ID for service-specific privileges to manage all features within the service.  
   *Examples: Exchange Administrator, Intune Administrator, SharePoint Administrator, Teams Administrator.*

3. **Cross-service roles in Microsoft Entra ID:**  
   Some roles span services, such as Global Administrator and Global Reader. All Microsoft 365 services honor these two roles. There are also security-related roles like Security Administrator and Security Reader that grant access across multiple security services within Microsoft 365.  
   *Examples: Security Administrator, Compliance Administrator.*

---

## Microsoft Entra Built-in Roles by Category

| Category                              | Roles                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Microsoft Entra ID-specific roles**  | Application Administrator, Application Developer, Authentication Administrator, B2C IEF Keyset Administrator, B2C IEF Policy Administrator, Cloud Application Administrator, Cloud Device Administrator, Conditional Access Administrator, Device Administrators, Directory Readers, Directory Synchronization Accounts, Directory Writers, External ID User Flow Administrator, External ID User Flow Attribute Administrator, Groups Administrator, Guest Inviter, Helpdesk Administrator, Hybrid Identity Administrator, License Administrator, Partner Tier1 Support, Partner Tier2 Support, Password Administrator, Privileged Authentication Administrator, Privileged Role Administrator, Reports Reader, User Administrator |
| **Service-specific roles**             | Azure DevOps Administrator, Azure Information Protection Administrator, Billing Administrator, CRM Service Administrator, Customer Lockbox Access Approver, Desktop Analytics Administrator, Exchange Service Administrator, Insights Administrator, Insights Business Leader, Intune Service Administrator, Kaizala Administrator, Lync Service Administrator, Message Center Privacy Reader, Message Center Reader, Modern Commerce Administrator, Network Administrator, Office Apps Administrator, Power BI Service Administrator, Power Platform Administrator, Printer Administrator, Printer Technician, Search Administrator, Search Editor, SharePoint Service Administrator, Teams Communications Administrator, Teams Communications Support Engineer, Teams Communications Support Specialist, Teams Devices Administrator, Teams Administrator |
| **Cross-service roles**                | Compliance Administrator, Compliance Data Administrator, Global Reader, Global Administrator, Security Administrator, Security Operator, Security Reader, Service Support Administrator                                                                                                                                                                                                                                 |

---

*The categories above are named for clarity and are not intended to imply any other capabilities beyond the documented Microsoft Entra role permissions.*

