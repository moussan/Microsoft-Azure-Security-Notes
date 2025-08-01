# Overview of Role-Based Access Control in Microsoft Entra ID

Microsoft Entra roles allow you to grant granular permissions to your admins, abiding by the principle of least privilege.

## Types of Role Definitions

Microsoft Entra ID supports two types of role definitions:

- **Built-in roles**
- **Custom roles**

### Built-in Roles

Built-in roles are out-of-the-box roles with a fixed set of permissions. These role definitions cannot be modified. There are many built-in roles that Microsoft Entra ID supports, and the list is growing.

### Custom Roles

To meet sophisticated requirements, Microsoft Entra ID also supports custom roles. Granting permission using custom Microsoft Entra roles is a two-step process:

1. **Create a custom role definition**  
   A custom role definition is a collection of permissions that you add from a preset list. These permissions are the same as those used in built-in roles.

2. **Assign the custom role**  
   Once you’ve created your custom role definition (or are using a built-in role), you can assign it to a user by creating a role assignment.  
   - A role assignment grants the user the permissions in a role definition at a specified scope.
   - This two-step process allows you to create a single role definition and assign it many times at different scopes.

## Scope

A scope defines the set of Microsoft Entra resources the role member has access to. The most common scope is organization-wide (org-wide) scope.

- A custom role can be assigned at org-wide scope, meaning the role member has the role permissions over all resources in the organization.
- A custom role can also be assigned at an object scope (e.g., a single application).

**Example:**  
The same role can be assigned to one user over all applications in the organization and to another user with a scope of only the Expense Reports app.