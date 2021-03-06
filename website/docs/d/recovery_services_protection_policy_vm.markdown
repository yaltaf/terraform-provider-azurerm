---
subcategory: "Recovery Services"
layout: "azurerm"
page_title: "Azure Resource Manager: azurerm_recovery_services_protection_policy_vm"
description: |-
  Gets information about an existing Recovery Services VM Protection Policy.
---

# Data Source: azurerm_recovery_services_protection_policy_vm

Use this data source to access information about an existing Recovery Services VM Protection Policy.

## Example Usage

```hcl
data "azurerm_recovery_services_protection_policy_vm" "policy" {
  name                = "policy"
  recovery_vault_name = "recovery_vault"
  resource_group_name = "resource_group"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) Specifies the name of the Recovery Services VM Protection Policy.

* `recovery_vault_name` - (Required) Specifies the name of the Recovery Services Vault.

* `resource_group_name` - (Required) The name of the resource group in which the Recovery Services VM Protection Policy resides.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the Recovery Services VM Protection Policy.

* `tags` - A mapping of tags assigned to the resource.


### Timeouts

~> **Note:** Custom Timeouts are available [as an opt-in Beta in version 1.43 of the Azure Provider](/docs/providers/azurerm/guides/2.0-beta.html) and will be enabled by default in version 2.0 of the Azure Provider.

The `timeouts` block allows you to specify [timeouts](https://www.terraform.io/docs/configuration/resources.html#timeouts) for certain actions:

* `read` - (Defaults to 5 minutes) Used when retrieving the Recovery Services VM Protection Policy.
