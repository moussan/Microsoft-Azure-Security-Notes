# Azure AD Privileged Identity Management (PIM)

## Introduction

Azure AD Privileged Identity Management (Azure AD PIM) is a crucial service within Azure. It assists in managing, controlling, and monitoring access within Azure AD, and is also beneficial for managing and monitoring privileged roles within the organization. In this reading, you will explore PIM’s various characteristics and discover how it links to the access lifecycle.

---

## What is Azure AD PIM?

Organizations have resources with unique security requirements. For example:

- **Azure Blob Storage container**: May contain public-related data.
- **Azure Virtual Network Gateway**: Collects sensitive network configuration and access information.

Role responsibility is tied to the sensitivity of the data or application. Access to sensitive objects is limited to exclusive roles.

**Privileged Identity Management (PIM)** is an Azure AD service that allows you to control access to sensitive network resources. This extends beyond Azure AD to other Microsoft services such as Intune, Microsoft 365, and Azure.  
"Privileged" refers to the level of access to a role that can alter a resource. Managing who can change what is fundamental to a solid security posture.

---

## Key Features of PIM

PIM helps offset excessive or unnecessary access requests by requiring justification. Before interacting with a resource, an employee may need elevated access, which can be temporarily granted. This can also apply to privileged actions, such as creating or deleting a resource.  
PIM enforces multi-factor authentication (MFA) to activate permissions. To manage PIM, you must be a **Global Administrator** or **Privileged Role Administrator**.

### PIM Traits

- **Just-in-time (JIT)**: Privileged access is only granted when required.
- **Time-bound**: Access requests have a start and end date, ensuring permissions do not linger after task completion.
- **Approval-based**: Access must be explicitly granted and monitored by a responsible guardian.
- **Visible**: Administrators are notified when a request is made, increasing transparency.
- **Auditable**: PIM resources maintain an audit trail of who accessed the resource, when permissions were allocated, who issued them, and actions performed while permissions were active.

Together, these features enhance security and governance by limiting when, how long, and by whom resources can be accessed, all monitored and protected with conditional access checks.

---

## Just-in-Time Access in PIM

Employees working on many projects may accumulate access over time. The **identity lifecycle** mechanism revokes privileges when tasks are completed. This is core to PIM and is known as **just-in-time (JIT) access**.

### Benefits of JIT Access

- Limits the impact of mistakes or compromised identities.
- Requires employees to request access, specifying duration and justification.
- Managers can review and approve requests, increasing oversight.
- MFA is required for activation.
- The process is documented, providing an audit trail.

### User States in PIM

- **Eligible**: The user is granted the right to use the role but must request activation.
- **Active**: The user is both eligible and currently has access to the resource.

---

How Microsoft Entra ID determines if a user has access to a resource
The following are the high-level steps that Microsoft Entra ID uses to determine if you have access to a management resource. Use this information to troubleshoot access issues.

A user (or service principal) acquires a token to the Microsoft Graph endpoint.
The user makes an API call to Microsoft Entra ID via Microsoft Graph using the issued token.
Depending on the circumstance, Microsoft Entra ID takes one of the following actions:
Evaluates the user’s role memberships based on the wids claim in the user’s access token.
Retrieves all the role assignments that apply for the user, either directly or via group membership, to the resource on which the action is being taken.
Microsoft Entra ID determines if the action in the API call is included in the roles the user has for this resource.
If the user doesn't have a role with the action at the requested scope, access is not granted. Otherwise access is granted.

Role assignment
A role assignment is a Microsoft Entra resource that attaches a role definition to a security principal at a particular scope to grant access to Microsoft Entra resources. Access is granted by creating a role assignment, and access is revoked by removing a role assignment. At its core, a role assignment consists of three elements:

Security principal - An identity that gets the permissions. It could be a user, group, or a service principal.
Role definition - A collection of permissions.
Scope - A way to constrain where those permissions are applicable.
You can create role assignments and list the role assignments using the Microsoft Entra admin center, Microsoft Graph PowerShell, or Microsoft Graph API. Azure CLI is not supported for Microsoft Entra role assignments.

Security principal
A security principal represents a user, group, or service principal that is assigned access to Microsoft Entra resources. A user is an individual who has a user profile in Microsoft Entra ID. A group is a new Microsoft 365 or security group that has been set as a role-assignable group. A service principal is an identity created for use with applications, hosted services, and automated tools to access Microsoft Entra resources.

### Role Definition

A **role definition** (or role) is a collection of permissions. A role definition lists the operations that can be performed on Microsoft Entra resources, such as create, read, update, and delete.

There are two types of roles in Microsoft Entra ID:

- **Built-in roles**: Created by Microsoft and can't be changed.
- **Custom roles**: Created and managed by your organization.

---

### Scope

A **scope** is a way to limit the permitted actions to a particular set of resources as part of a role assignment.  
For example, if you want to assign a custom role to a developer, but only to manage a specific application registration, you can include the specific application registration as a scope in the role assignment.

When you assign a role, you specify one of the following types of scope:

- **Tenant**
- **Administrative unit**
- **Microsoft Entra resource**

If you specify a Microsoft Entra resource as a scope, it can be one of the following:

- Microsoft Entra groups
- Enterprise applications
- Application registrations

> When a role is assigned over a container scope (such as the Tenant or an Administrative Unit), it grants permissions over the objects they contain but not on the container itself.  
> When a role is assigned over a resource scope, it grants permissions over the resource itself but does not extend beyond (in particular, it does not extend to the members of a Microsoft Entra group).

---

### Role Assignment Options

Microsoft Entra ID provides multiple options for assigning roles:

- **Direct assignment to users**:  
  The default way to assign roles. Both built-in and custom Microsoft Entra roles can be assigned to users, based on access requirements.  
  For more information, see *Assign Microsoft Entra roles*.

- **Role-assignable groups (Microsoft Entra ID P1)**:  
  You can create role-assignable groups and assign roles to these groups. Assigning roles to a group instead of individuals allows for easy addition or removal of users from a role and creates consistent permissions for all members of the group.  
  For more information, see *Assign Microsoft Entra roles*.

- **Privileged Identity Management (Microsoft Entra ID P2)**:  
  Use Microsoft Entra Privileged Identity Management (PIM) to provide just-in-time access to roles. This feature allows you to grant time-limited access to a role to users who require it, rather than granting permanent access. It also provides detailed reporting and auditing capabilities.  
  For more information, see *Assign Microsoft Entra roles in Privileged Identity Management*.

---

### License Requirements

- Using built-in roles in Microsoft Entra ID is **free**.
- Using custom roles requires a **Microsoft Entra ID P1 license** for every user with a custom role assignment.