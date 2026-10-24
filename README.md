# CloudLink — AWS VPC Peering Project

## Project Overview

CloudLink is a hands-on AWS networking project that demonstrates how two Amazon Virtual Private Clouds (VPCs) can be connected using VPC Peering.

The project is configured manually through the AWS Management Console.

## Objectives

- Create two separate VPCs.
- Configure subnets and route tables.
- Establish a VPC peering connection.
- Configure reciprocal routes between the VPCs.
- Create security groups.
- Document the configuration with screenshots.

## Architecture

| Resource | Configuration |
|---|---|
| VPC A | `CloudLink-VPC-A` |
| VPC A CIDR | `10.0.0.0/16` |
| Subnet A | `CloudLink-Subnet-A` |
| Subnet A CIDR | `10.0.1.0/24` |
| Route table A | `CloudLink-RT-A` |
| Security group A | `CloudLink-SG-A` |
| VPC B | `CloudLink-VPC-B` |
| VPC B CIDR | `10.1.0.0/16` |
| Subnet B | `CloudLink-Subnet-B` |
| Subnet B CIDR | `10.1.1.0/24` |
| Route table B | `CloudLink-RT-B` |
| Security group B | `CloudLink-SG-B` |
| Peering connection | `CloudLink-Peering` |
| AWS Region | Asia Pacific (Sydney), `ap-southeast-2` |

## Routing Configuration

- VPC A route table: destination `10.1.0.0/16` through the VPC peering connection.
- VPC B route table: destination `10.0.0.0/16` through the VPC peering connection.
- Each VPC retains its local route.

## Security

Separate security groups are created for the two VPCs. Inbound rules are intentionally left empty until specific communication requirements are defined.

## Validation Status

The peering connection was reported as Active, and both route tables were reported as showing the intended routes.

End-to-end application connectivity has not yet been tested.

## Cost Considerations

The project avoids unnecessary compute resources and focuses on VPC networking configuration. AWS charges should be checked before provisioning additional services.

## Screenshots

Screenshots of the VPCs, subnets, peering connection, route tables, and security groups are intended to document the implementation.

## Future Improvements

- Add a verified architecture diagram.
- Perform a connectivity test using suitable endpoints if cost permits.
- Record the actual test results.
- Expand the implementation report and viva questions.

## Author
Pakki Kranthi Kumar
