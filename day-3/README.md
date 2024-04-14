# What will you learn 

## Introduction to EC2:

What is EC2, and why is it important?

```
- Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.
- Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.
- Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.
- Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.
```

EC2 usecases

```
Deliver secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.
Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively.
Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing.
Deliver the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects
```

EC2 Instance Types

Recommended to follow [this](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) page for very detailed and updated information.

General purpose

```
General Purpose instances are designed to deliver a balance of compute, memory, and network resources. They are suitable for a wide range of applications, including web servers,
small databases, development and test environments, and more.
```

Compute optimized

```
Compute Optimized instances provide a higher ratio of compute power to memory. They excel in workloads that require high-performance processing such as batch processing, 
scientific modeling, gaming servers, and high-performance web servers.
```

Memory optimized

```
Memory Optimized instances are designed to handle memory-intensive workloads. They are suitable for applications that require large amounts of memory, such as in-memory databases,
real-time big data analytics, and high-performance computing.
```

Storage optimized

```
Storage Optimized instances are optimized for applications that require high, sequential read and write access to large datasets. 
They are ideal for tasks like data warehousing, log processing, and distributed file systems.
```

Accelerated computing

```
Accelerated Computing Instances typically come with one or more types of accelerators, such as Graphics Processing Units (GPUs),
Field Programmable Gate Arrays (FPGAs), or custom Application Specific Integrated Circuits (ASICs). 
These accelerators offload computationally intensive tasks from the main CPU, enabling faster and more efficient processing for specific workloads.
```

![image](https://github.com/iam-veeramalla/aws-devops-zero-to-hero/assets/43399466/fc8e083c-dba5-41a6-94b9-14ebef0255c1)

Instance families

```
    C – Compute

    D – Dense storage

    F – FPGA

    G – GPU

    Hpc – High performance computing

    I – I/O

    Inf – AWS Inferentia

    M – Most scenarios

    P – GPU

    R – Random access memory

    T – Turbo

    Trn – AWS Tranium

    U – Ultra-high memory

    VT – Video transcoding

    X – Extra-large memory
```

Additional capabilities

```
    a – AMD processors

    g – AWS Graviton processors

    i – Intel processors

    d – Instance store volumes

    n – Network and EBS optimized

    e – Extra storage or memory

    z – High performance
```

## EC2 Instance Basics:

Understanding the concept of virtual servers and instances.
Key components of an EC2 instance: AMI (Amazon Machine Image), instance types, and instance states.
Differentiating between On-Demand, Reserved, and Spot instances.

## Launching an EC2 Instance:

- Step-by-step guide on launching an EC2 instance using the AWS Management Console.
- Configuring instance details, such as instance type, network settings, and storage options.
- Understanding security groups and key pairs for securing instances.

## Managing EC2 Instances:

- Starting, stopping, and terminating instances.
- Monitoring instance performance and utilization.
- Basic troubleshooting and accessing instances using SSH (Secure Shell).

- Amazon EC2 (Elastic Compute Cloud) is one of the core services offered by Amazon Web Services (AWS). It provides resizable compute capacity in the cloud, allowing users to run virtual machines, known as instances, to host their applications or workloads. Here's a rundown of its features:

Scalability: EC2 allows you to scale your compute capacity up or down based on your application requirements. You can easily add or remove instances as needed, helping you to manage fluctuating workloads efficiently.

Variety of Instance Types: EC2 offers a wide range of instance types optimized for different use cases, such as compute-optimized, memory-optimized, storage-optimized, and GPU instances. This allows you to choose the instance type that best suits your application's requirements in terms of CPU, memory, storage, and networking resources.

Pay-As-You-Go Pricing: With EC2, you pay only for the compute capacity that you use, on an hourly or per-second basis, depending on the instance type. This pay-as-you-go pricing model helps you optimize costs by scaling your infrastructure according to demand.

Flexibility: EC2 provides flexibility in terms of operating systems, networking configurations, security settings, and storage options. You can choose from a variety of operating systems, including Amazon Linux, Ubuntu, Windows Server, and others, and customize your instances to meet your specific requirements.

Integration with Other AWS Services: EC2 integrates seamlessly with other AWS services, such as Amazon S3 (Simple Storage Service), Amazon RDS (Relational Database Service), Amazon VPC (Virtual Private Cloud), and AWS IAM (Identity and Access Management), enabling you to build complex, scalable, and secure applications.

Elastic Load Balancing and Auto Scaling: EC2 works in conjunction with Elastic Load Balancing (ELB) and Auto Scaling to distribute incoming traffic across multiple instances and automatically adjust the number of instances based on demand. This ensures high availability, fault tolerance, and optimal performance for your applications.

Security: EC2 provides several security features, including security groups, network access control lists (ACLs), and key pairs, to help you secure your instances and data. You can control access to your instances by defining rules that govern inbound and outbound traffic, and you can encrypt data at rest and in transit using various encryption options.

Overall, Amazon EC2 is a powerful and versatile service that allows you to deploy and manage virtual servers in the cloud with ease, providing the flexibility, scalability, and reliability needed to run a wide range of applications and workloads.
