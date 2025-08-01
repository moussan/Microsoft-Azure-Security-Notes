# Microsoft Entra Built‑in Roles & Permissions Reference (2025‑07‑25)

## Overview

* Microsoft Entra ID built‑in roles assign permissions to manage directory objects (users, groups, apps), networks, identity providers, reporting, and more ([Microsoft Learn][1]).
* Each role defines a fixed set of actions and cannot be modified. Roles can be assigned at various scopes (tenant, administrative units, app registration) ([Microsoft Learn][1]).

---

## Roles & Sample Permissions

Below is a selection of built‑in roles with a brief description of key permissions:

| Role Name                             | Description / Scope                                                                                | Sample Permissions (Actions)                                                                                               |
| ------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Global Administrator**              | Full control over Microsoft Entra ID and services (M365, Defender, Purview, Azure subscriptions)   | Access to all admin features, reset passwords, manage network access, view reports and sign‑in logs ([Microsoft Learn][1]) |
| **Security Administrator**            | Manage security features (M365 Defender, Entra ID Protection, compliance portal)                   | Manage alerts, security policies; most Security Reader permissions; *does not manage roles* ([Microsoft Learn][1])         |
| **Helpdesk Administrator**            | Reset user passwords, invalidate sessions, limited directory support                               | Password reset, invalidate refresh tokens, view basic portal service health ([Microsoft Learn][1])                         |
| **Compliance Administrator**          | Manage compliance tools across Purview, Defender, M365 admin center                                | Manage compliance features, support tickets, Service Health, compliance manager actions ([Microsoft Learn][1])             |
| **Insights Administrator**            | Full access to Viva Insights app                                                                   | Manage Analytics queries, service health, support tickets, portal read access ([Microsoft Learn][1])                       |
| **Insights Analyst**                  | Read-only analytical access in Viva Insights                                                       | Run queries; limited portal access; support tickets but no config changes ([Microsoft Learn][1])                           |
| **Application Administrator**         | Create/manage app registrations and enterprise apps                                                | Directory app creation, registration, assignment tasks ([Microsoft Learn][1])                                              |
| **Attribute Definition/Reader/Admin** | Manage or read custom security attribute definitions and assignments                               | Define attribute schema; read or assign attributes; apply attributes to directory objects ([Microsoft Learn][1])           |
| **Identity Governance Administrator** | Manage identity governance workflows (entitlement management, access packages, lifecycle policies) | Full access to governance scenarios and entitlement management features ([Microsoft Learn][1])                             |
| **Fabric Administrator**              | Manage Microsoft Fabric and Power BI support issues                                                | Manage Fabric/Power BI; support tickets; Azure Service Health ([Microsoft Learn][1])                                       |

---

## Additional Role Categories

* **Microsoft Entra Joined Device Local Administrator** — becomes local admin on Azure‑joined Windows 10 devices; cannot manage devices via Entra ID ([Microsoft Learn][1])
* **Microsoft Graph Data Connect Administrator** — manage Graph Data Connect workload, authorizations, cross‑tenant movements ([Microsoft Learn][1])
* **Hardware Warranty Administrator/Specialist** — manage Microsoft hardware warranty claims and related support workflows ([Microsoft Learn][1])
* **Permissions Management Administrator** — full control over Permissions Management in Entra when available; can assign Entra roles ([Microsoft Learn][1])
* **Search Administrator / Search Editor** — manage Microsoft Search content (bookmarks, Q\&A, locations) and read message center, support tickets ([Microsoft Learn][1])

---

## Related Concepts & Best Practices

* **Least Privilege**: Always assign the minimum necessary permissions, limited to specific roles, scopes, and time periods. Use Privileged Identity Management (PIM) for just‑in‑time role activation and automatic de‑activation after time-limited assignments ([Microsoft Learn][2], [Microsoft Learn][3]).
* **Scopes**: Roles can be scoped to the entire tenant or narrowed down using administrative units or application registrations ([Microsoft Learn][4]).
* **Privileged Permissions**: Roles marked as “Privileged” allow sensitive operations like delegation, credential modification, or access to restricted data. Use caution when assigning these roles ([Microsoft Learn][5]).

---

This Markdown digest captures essential details from the official *Permissions Reference* including role definitions, sample permissions, and recommendations. For the full list of permissions associated with each built‑in role, please consult the original Microsoft Learn page ([Microsoft Learn][6]).

[1]: https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference?utm_source=chatgpt.com "Microsoft Entra built-in roles"
[2]: https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/best-practices?utm_source=chatgpt.com "Best practices for Microsoft Entra roles"
[3]: https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/custom-overview?utm_source=chatgpt.com "Overview of role-based access control in Microsoft Entra ID"
[4]: https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/manage-roles-portal?utm_source=chatgpt.com "Assign Microsoft Entra roles"
[5]: https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/privileged-roles-permissions?utm_source=chatgpt.com "Privileged roles and permissions in Microsoft Entra ID (preview)"
[6]: https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles?utm_source=chatgpt.com "Azure built-in roles - Azure RBAC | Microsoft Learn"
