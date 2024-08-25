# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.



AWS Cloud Cost Optimization is the process of reducing unnecessary cloud expenditures while maintaining performance, availability, and functionality. It involves analyzing and managing various aspects of your AWS environment to ensure that resources are used efficiently, leading to cost savings. Cost optimization is essential because it helps businesses manage their cloud spending effectively, avoid overprovisioning, and leverage the flexibility of AWS services to pay only for what they need.

Key Strategies for AWS Cloud Cost Optimization
Right-Sizing Resources: Adjusting the size of your compute instances (EC2) to match actual demand. Over-provisioned instances can lead to wasted resources and unnecessary costs.

Reserved Instances (RIs) and Savings Plans: Committing to a one- or three-year term for certain resources at a lower price compared to on-demand pricing. This is beneficial for workloads with predictable usage patterns.

Auto Scaling: Implementing auto-scaling to dynamically adjust the number of running instances based on demand, ensuring that you only pay for the compute power you need.

Use of Spot Instances: Leveraging spot instances for non-critical workloads. These are available at a discount compared to on-demand instances but can be interrupted by AWS.

Optimizing Storage Costs: Utilizing different storage classes (e.g., S3 Standard, S3 Intelligent-Tiering, S3 Glacier) based on the access frequency and data lifecycle. This ensures that you're not paying premium prices for data that is rarely accessed.

Monitoring and Alerts: Using AWS Cost Explorer, CloudWatch, and other tools to monitor spending, set budgets, and receive alerts when costs exceed predefined thresholds.

Consolidating and Archiving Logs: Using tools like Amazon S3 to store logs in a more cost-effective way, rather than keeping them in expensive, high-performance storage.

Rightsizing Database Instances: Optimizing RDS instances or migrating to Aurora Serverless for variable database workloads.

Real-Time Example
Scenario: Migrating a Web Application to AWS

Imagine a company that has recently migrated its web application from an on-premises data center to AWS. Initially, they provision large EC2 instances and allocate standard storage to handle peak traffic based on their historical data. However, they notice that their monthly AWS bill is higher than expected.

Steps for Cost Optimization:

Analyze Compute Utilization: Using AWS Cost Explorer and CloudWatch, they observe that the EC2 instances are underutilized during off-peak hours. The company decides to implement Auto Scaling to adjust the number of instances based on real-time traffic, reducing costs during low-traffic periods.

Move to Reserved Instances: The company identifies consistent usage patterns for certain workloads and purchases Reserved Instances to save up to 75% compared to on-demand pricing.

Leverage Spot Instances: For non-critical background processing tasks, they start using Spot Instances, which cost significantly less than on-demand instances.

Storage Optimization: The company notices that a large amount of data stored in S3 is rarely accessed. They move this data to S3 Glacier, a lower-cost storage option, and enable S3 Intelligent-Tiering for frequently accessed data.

Database Cost Optimization: They evaluate their RDS usage and switch to Aurora Serverless for certain variable workloads, ensuring that they only pay for database capacity when it's in use.

Monitoring and Alerts: The company sets up CloudWatch Alarms to monitor costs and receive alerts if spending approaches their budget, enabling them to take proactive measures to control costs.

By following these optimization strategies, the company significantly reduces its monthly AWS bill while maintaining the performance and reliability of its web application.






