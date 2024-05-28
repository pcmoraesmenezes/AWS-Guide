# AWS - RDS (Relational Database Service)

## Introduction

RDS is a managed relational database service in aws that provides you six popular database engines to choose from, including Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, and Microsoft SQL Server.

RDS is considered a managed service because AWS handles the provisioning, setup, and maintenance of the database, which allows you to focus on your application and data. Also the common database administration tasks like backups, software patching, monitoring, scaling, and replication are managed by AWS.

Shell access is not provided to RDS instances, because is a managed service, so you can't log in to the instances and perform tasks like you would on a self-managed database server.

### RDS Characteristics

The capacity depends on the DB Engine and can be scaled up or down based on your needs. You can also choose the instance type, storage type, and storage size.

RDS provides some options like **Supports Magnetic**, **General Purpose (SSD)**, and **Provisioned IOPS (SSD)** storage types.

#### Supports Magnetic

This option is the most economical and older storage type. It is recommended for small database workloads where data is accessed less frequently. 

The I/O performance is very limited and the performance is not consistent.

#### General Purpose (SSD)

This option is based on SSDs storages and offer an balance beetwen price and performance. Also use a credit system to burst performance.

The I/O performance is consistent and the performance is good for most of the workloads.

#### Provisioned IOPS (SSD)

This option is used for high-performance database workloads. When the I/O charge is critical, this choice is the best.

The I/O performance is consistent and the performance is the best for high-performance database workloads.

---

RDS Instances can run inside a VPC (Virtual Private Cloud) and you can control the network access to the instances using security groups.

#### What's a VPC?

A VPC is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.

The default VPC is not safe, so you should create a custom VPC and configure the security groups to control the network access to the RDS instances.

---

We can monitored the RDS instances using CloudWatch, which is a monitoring service for AWS Cloud resources and the applications you run on AWS.

Use EBS (Elastic Block Store) volumes to store the data of the RDS instances. EBS volumes are network-attached storage that you can attach to your instances. This supports a auto-scaling feature.

#### Gerenal Purpose of EBS

1. Persistence Storage

2. High Availability

3. Backup and Restore

4. Flexibility and Scalability

---

### RDS Billing

The RDS billing is based on the following factors:

1. Based on instance type and database engine

2. Storage

3. I/O requests

4. Backup storage

5. Data transfer