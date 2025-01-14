---
subcategory: "OpenSearch Serverless"
layout: "aws"
page_title: "AWS: aws_opensearchserverless_vpc_endpoint"
description: |-
  Terraform data source for managing an AWS OpenSearch Serverless VPC Endpoint.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_opensearchserverless_vpc_endpoint

Terraform data source for managing an AWS OpenSearch Serverless VPC Endpoint.

## Example Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsOpensearchserverlessVpcEndpoint } from "./.gen/providers/aws/data-aws-opensearchserverless-vpc-endpoint";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataAwsOpensearchserverlessVpcEndpoint(this, "example", {
      vpcEndpointId: "vpce-829a4487959e2a839",
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `vpcEndpointId` - (Required) The unique identifier of the endpoint.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `createdDate` - The date the endpoint was created.
* `name` - The name of the endpoint.
* `securityGroupIds` - The IDs of the security groups that define the ports, protocols, and sources for inbound traffic that you are authorizing into your endpoint.
* `subnetIds` - The IDs of the subnets from which you access OpenSearch Serverless.
* `vpcId` - The ID of the VPC from which you access OpenSearch Serverless.

<!-- cache-key: cdktf-0.20.0 input-2c446629971d0d10ff448173c283856675b8628bf661beac57c916ae51592d6d -->