You can automate the creation, retention, and deletion of EBS snapshots using Amazon Data Lifecycle Manager. Amazon Data Lifecycle Manager can schedule snapshots during off-peak hours to minimize performance impact and automatically delete outdated backups to control storage costs. It's particularly valuable for large-scale deployments where manual snapshot management would be time-consuming and error-prone.

To learn how you can use Data Lifecycle Manager to create custom EBS Snapshots policies, choose the arrow buttons to display each of the following five steps.

### Amazon Data Lifecycle Manager Workflow

By reducing manual effort and establishing consistent backup policies, Amazon Data Lifecycle Manager helps maintain compliance requirements by scheduling regular backups and enforcing retention rules.


## STEPS

#### Create an EBS snapshots policy

Create an EBS snapshots policy using the Amazon EC2 console, API calls, AWS Command Line Interface (AWS CLI), SDKs, or AWS CloudFormation.

#### Select target resource type
Choose either an EBS volume or an EC2 instance as the target for the snapshot.

#### Exclude volumes
Narrow down the data to be included in the snapshot by choosing options to exclude either the root volume or data volumes.

#### Set custom schedules
Automate the creation, retention, and deletion of EBS snapshots by setting up custom schedules.

#### Apply additional actions
Before finalizing the policy, you can apply additional actions. These include configuring elements of the snapshots like tags, snapshot archiving, Amazon EBS fast snapshot restore, cross-Region copying, and cross-account sharing.