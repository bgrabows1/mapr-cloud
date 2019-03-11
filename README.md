# mapr-cloud
Repository contains mapr cloud related files (CloudFormation mostly) for AWS public provider.

 
## Prerequisites
To run the provisioning templates you have to have the following permissions to create IAM objects in AWS:
-   `iam:GetRole`
-   `iam:PassRole`
-   `iam:PutRolePolicy`
-   `iam:CreateRole`
-   `iam:AddRoleToInstanceProfile`
-   `iam:CreateInstanceProfile`
  
## Steps for Deploying Using a Marketplace Offering
Use these steps to deploy a cluster using one of the MapR Marketplace offerings for AWS:

1.  Find MapR in the **AWS Marketplace**.
2.  Click the title of the MapR offering that you want to use. AWS displays product overview and pricing information for you to review.
3.  Set the region and EC2 instance type.
4.  Click **Continue to Subscribe**. The Subscribe to this software page appears.
5.  Click **Continue to Configuration**. The Configure this software page appears.
6.  In the Fulfillment Option field, select **MapR Standard Cluster with VPC Support**.
7.  Click **Continue to launch**. The Launch this software page appears.
8.  Under Choose Action, select **Launch CloudFormation.**
9.  Click **Launch**. The Create Stack page is displayed. By default an Amazon S3 Template URL option is selected, and the URL for the MapR template is prefilled in the URL field.
10.  Click **Next**. The MapR CloudFormation template should appear.
11.  Fill in the template.

## Filling the Template
**stack name** - The stack name cannot contain spaces.

**clusterAdminPassword** - Password you will use to log into the MCS or the MapR Installer.

**MEP** - Select MapR Exosystem Pack version.

**provisioningTemplate** - List of auto-provisioning templates.

**nodeCount** - Specify the number of nodes in the cluster.

**InstallerOnitsOwn** - Select true to configure MapR Installer on a node that is not part of the cluster.

**instanceType** - MapR supprted instance types in AWS.

**useinstanceStore** - Set to true if machine type supports instance stores (ephemeral disks).

**diskCount** - Number of disks per node.

**diskType** - Specify the disk type.

**diskSize** - Specify the disk size.

**keyName** - Specify the keypair.

**useExistingSubnet** - Leave empty if you would like a new VPC and subnets created.

**securityGroups** - Leave this empty to create a new VPN and subnets.

**assignPublicIP** - Set true if you want to assign public IP to each node.

**publicAccessCIDR** - Specify an IP range you want to restrict from which the stack can be accessed. 
