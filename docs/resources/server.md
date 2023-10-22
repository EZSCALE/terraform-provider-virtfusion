---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "virtfusion_server Resource - terraform-provider-virtfusion"
subcategory: ""
description: |-
  Virtfusion Server Resource
---

# virtfusion_server (Resource)

Virtfusion Server Resource

## Example Usage

```terraform
resource "virtfusion_server" "node1" {
  package_id             = 1
  user_id                = 1
  hypervisor_id          = 1
  ipv4                   = 1
  storage                = 30
  memory                 = 1024
  cores                  = 1
  traffic                = 1000
  inbound_network_speed  = 100
  outbound_network_speed = 100
  storage_profile        = 1
  network_profile        = 1
  name                   = "test"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `hypervisor_id` (Number) Hypervisor Group ID
- `package_id` (Number) Package ID
- `user_id` (Number) User ID

### Optional

- `cores` (Number) How many cores to allocate. Omit to use the default core count from the package.
- `inbound_network_speed` (Number) Inbound network speed in kB/s. Omit to use the default inbound network speed from the package.
- `ipv4` (Number) IPv4 Addresses to assign. Omit to use the default of 1 IPv4.
- `memory` (Number) How much memory to allocate in MB. Omit to use the default memory size from the package.
- `name` (String) Server name. If omitted, a random UUID will be generated.
- `network_profile` (Number) Network profile ID. Omit to use the default network profile from the package.
- `outbound_network_speed` (Number) Outbound network speed in kB/s. Omit to use the default outbound network speed from the package.
- `storage` (Number) Primary storage size in GB. Omit to use the default storage size from the package.
- `storage_profile` (Number) Storage profile ID. Omit to use the default storage profile from the package.
- `traffic` (Number) How much traffic to allocate in GB. Omit to use the default traffic size from the package. 0=Unlimited

### Read-Only

- `id` (Number) Server ID