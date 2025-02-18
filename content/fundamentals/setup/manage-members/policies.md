---
pcx_content_type: reference
title: Policies
weight: 3
meta:
    title: Policies
---

# Policies

Policies define what access a given user has to your account or domains, and are constructed out of three parts:

1. An actor (your user).
2. A `ResourceGroup` (a scope).
3. A `PermissionGroup` (roles).

An account member can have one or several of these policies to represent the most appropriate access.

To increase the usability and flexibility of Cloudflare's role system, changes to the API have been made to expose these underlying data principles and allow users to interact with them.

For example, you may want to assign multiple policies and use scopes to control access to an account where you have a single account with both Production and Staging domains, and a user that should be able see the whole account, purge the production domains, but have the ability to configure the staging domains.

## Manage policies

A set of standard API endpoints is present on every account that allow access to your members, which has recently been enhanced by a list of `resourceGroups` and `PermissionGroups`.

- A `resourceGroup` is a unique identifier for the scope for which a policy applies.
- A `permissionGroup` is a unique identifier for the set of roles that are assigned to a given policy.

Refer to the [API documentation](/api/) for more information.