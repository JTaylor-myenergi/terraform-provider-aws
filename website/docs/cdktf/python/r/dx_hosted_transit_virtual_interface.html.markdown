---
subcategory: "Direct Connect"
layout: "aws"
page_title: "AWS: aws_dx_hosted_transit_virtual_interface"
description: |-
  Provides a Direct Connect hosted transit virtual interface resource.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_dx_hosted_transit_virtual_interface

Provides a Direct Connect hosted transit virtual interface resource.
This resource represents the allocator's side of the hosted virtual interface.
A hosted virtual interface is a virtual interface that is owned by another AWS account.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import Token, TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.dx_hosted_transit_virtual_interface import DxHostedTransitVirtualInterface
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name, *, ownerAccountId):
        super().__init__(scope, name)
        DxHostedTransitVirtualInterface(self, "example",
            address_family="ipv4",
            bgp_asn=65352,
            connection_id=Token.as_string(aws_dx_connection_example.id),
            name="tf-transit-vif-example",
            vlan=4094,
            owner_account_id=owner_account_id
        )
```

## Argument Reference

This resource supports the following arguments:

* `address_family` - (Required) The address family for the BGP peer. `ipv4 ` or `ipv6`.
* `bgp_asn` - (Required) The autonomous system (AS) number for Border Gateway Protocol (BGP) configuration.
* `connection_id` - (Required) The ID of the Direct Connect connection (or LAG) on which to create the virtual interface.
* `name` - (Required) The name for the virtual interface.
* `owner_account_id` - (Required) The AWS account that will own the new virtual interface.
* `vlan` - (Required) The VLAN ID.
* `amazon_address` - (Optional) The IPv4 CIDR address to use to send traffic to Amazon. Required for IPv4 BGP peers.
* `bgp_auth_key` - (Optional) The authentication key for BGP configuration.
* `customer_address` - (Optional) The IPv4 CIDR destination address to which Amazon should send traffic. Required for IPv4 BGP peers.
* `mtu` - (Optional) The maximum transmission unit (MTU) is the size, in bytes, of the largest permissible packet that can be passed over the connection. The MTU of a virtual transit interface can be either `1500` or `8500` (jumbo frames). Default is `1500`.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - The ID of the virtual interface.
* `arn` - The ARN of the virtual interface.
* `aws_device` - The Direct Connect endpoint on which the virtual interface terminates.
* `jumbo_frame_capable` - Indicates whether jumbo frames (8500 MTU) are supported.

## Timeouts

[Configuration options](https://developer.hashicorp.com/terraform/language/resources/syntax#operation-timeouts):

- `create` - (Default `10m`)
- `update` - (Default `10m`)
- `delete` - (Default `10m`)

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import Direct Connect hosted transit virtual interfaces using the VIF `id`. For example:

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
```

Using `terraform import`, import Direct Connect hosted transit virtual interfaces using the VIF `id`. For example:

```console
% terraform import aws_dx_hosted_transit_virtual_interface.test dxvif-33cc44dd
```

<!-- cache-key: cdktf-0.20.0 input-f81c32393a3d19d17be728198b387816f13df0e65ec9958f05a3ac37f50db5bd -->