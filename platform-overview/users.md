---
description: Types of users
---

# Users

Every registered user is always a part of an Organization, even if it's just a single-person organization. Such structure enables [multi-tenancy](multi-tenant-tree-structure.md).  Within the organization there can be different types of users:

**Developer:** users of this type has access to all the functionality required to configure the platform for use by end-users \(also called Clients\). This is usually someone who builds the hardware, develops the firmware and does all the needed configurations. 

By default, a first user in organization ****becomes a Developer

{% hint style="info" %}
Currently, only one one developer is allowed per Organization to avoid sync issues. This limit might be changed later.
{% endhint %}

\*\*\*\*

**End-users \(also Clients\):** these users can add devices and use platform's functionality based on their role and set of permissions, but they can't edit any configurations made by Developer.



**Partner:** available in Enterprise version only. These are the members of Partners organization with additional set of functionality to create and manage clients. Partners could be: 

* Distributor 
* Reseller 
* Contractor 
* Installer

{% hint style="info" %}
Types of users are related to, but different from [Roles and Permission](../web-dashboard/for-developers/settings/access.md). 
{% endhint %}



\*\*\*\*

