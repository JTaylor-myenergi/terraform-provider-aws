---
subcategory: "RDS (Relational Database)"
layout: "aws"
page_title: "AWS: aws_rds_certificate"
description: |-
  Information about an RDS Certificate.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_rds_certificate

Information about an RDS Certificate.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_rds_certificate import DataAwsRdsCertificate
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsRdsCertificate(self, "example",
            latest_valid_till=True
        )
```

## Argument Reference

This data source supports the following arguments:

* `id` - (Optional) Certificate identifier. For example, `rds-ca-2019`.
* `latest_valid_till` - (Optional) When enabled, returns the certificate with the latest `ValidTill`.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `arn` - ARN of the certificate.
* `certificate_type` - Type of certificate. For example, `CA`.
* `customer_override` - Boolean whether there is an override for the default certificate identifier.
* `customer_override_valid_till` - If there is an override for the default certificate identifier, when the override expires.
* `thumbprint` - Thumbprint of the certificate.
* `valid_from` - [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8) of certificate starting validity date.
* `valid_till` - [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8) of certificate ending validity date.

<!-- cache-key: cdktf-0.20.0 input-11fac79b0d201c3f0e3fe5f7ce9e1273fd98f100c84dc2f6a4a3f5286bb6b1dd -->