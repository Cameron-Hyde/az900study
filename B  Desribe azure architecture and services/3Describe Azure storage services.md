# Introduction #

## Upon completing this module, you’ll be able to:
>Compare Azure storage services.
>Describe storage tiers.
>Describe redundancy options.
>Describe storage account options and storage types.
>Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync.
>Describe migration options, including Azure Migrate and Azure Data Box.

# Describe Azure storage accounts #

* A storage account provides a unique namespace for Azure Storage data that is accessible globally through HTTP or HTTPS
* Different types of storage accounts determine the storage services and redundancy options available
* Redundancy options include: Locally redundant storage (LRS), Geo-redundant storage (GRS), Read-access geo-redundant storage (RA-GRS), Zone-redundant storage (ZRS), Geo-zone-redundant storage (GZRS), and Read-access geo-zone-redundant storage (RA-GZRS)
* Standard general-purpose v2 storage accounts are recommended for most scenarios using Azure Storage and support Blob Storage, Queue Storage, Table Storage and Azure Files
* Premium storage accounts are recommended for high-transaction scenarios or those that require low storage latency
* Storage account names must be unique within Azure and are used to form the endpoint for accessing Azure Storage services
* Different storage services have different endpoint formats, such as: `https://<storage-account-name>.blob.core.windows.net for Blob Storage`, `https://<storage-account-name>.file.core.windows.net` for Azure Files, and so on
* Azure storage account has different type of storage to support for different needs like block blob, page blob and file share.
* Azure also provides different type of redundancy options to support for different data durability and availability scenarios.
* Azure also provides different types of migration options like AzCopy, Azure Storage Explorer, Azure File Sync, Azure Migrate and Azure Data Box to move data from on-premises to cloud or between different cloud storage services.

# Describe Azure storage redundancy #

* Azure Storage always stores multiple copies of data to protect against planned and unplanned events such as hardware failures, network or power outages, and natural disasters.
* When deciding which redundancy option to use, consider tradeoffs between lower costs and higher availability.    * Data in an Azure Storage account is always replicated three times in the primary region.
* Azure Storage offers two options for how data is replicated in the primary region: locally redundant storage (LRS) and zone-redundant storage (ZRS).
* LRS replicates data three times within a single data center in the primary region and offers at least 11 nines of durability (99.999999999%) of objects over a given year.
* LRS is the lowest-cost redundancy option and offers the least durability compared to other options, but protects data against server rack and drive failures.
* ZRS replicates data synchronously across three Azure availability zones in the primary region and offers at least 12 nines of durability (99.9999999999%) over a given year.
* ZRS is recommended for high availability and data governance requirements.
* For high durability, data can be additionally copied to a secondary region that is hundreds of miles away from the primary region.
* Azure Storage offers two options for copying data to a secondary region: geo-redundant storage (GRS) and geo-zone-redundant storage (GZRS).
* GRS copies data synchronously three times within a single physical location in the primary region and asynchronously to a single physical location in the secondary region.
* GZRS combines the high availability provided by ZRS in the primary region with protection from regional outages provided by geo-replication.
* By default, data in the secondary region is not available for read or write access unless there's a failover to the secondary region.
* Recovery point objective (RPO) indicates the point in time to which data can be recovered and Azure Storage typically has an RPO of less than 15 minutes.

# Describe Azure storage services #

* Azure Storage platform includes data services such as Azure Blobs (massively scalable object store for text and binary data), Azure Files (managed file shares for cloud or on-premises deployments), Azure Queues (messaging store for reliable messaging between application components), Azure Disks (block-level storage volumes for Azure VMs).
* Benefits of Azure Storage: durable and highly available, secure, scalable, managed, accessible.
* Azure Blob Storage is an object storage solution for the cloud that can store massive amounts of data, unstructured and can manage thousands of simultaneous uploads, ideal for serving images or documents directly to a browser, storing files for distributed access, streaming video and audio, storing data for backup and restore, disaster recovery, and archiving, and storing data for analysis by an on-premises or Azure-hosted service.
* Objects in Blob storage can be accessed from anywhere via HTTP or HTTPS, using URLs, the Azure Storage REST API, Azure PowerShell, Azure CLI, or Azure Storage client library.
* Azure provides different access tiers for Blob storage: Hot (optimized for frequently accessed data), Cool (optimized for infrequently accessed data stored for at least 30 days), and Archive (for rarely accessed data stored for at least 180 days)
* Azure Files offers fully managed file shares in the cloud accessible via SMB protocol, support for SMB 3.0 and NFSv3, accessible from on-premises, on VMs and in the cloud, supports Azure AD authentication, and can be used for scenarios such as home directories, shared content, and lift and shift of file-based workloads.
* Azure Queue Storage is a service for storing large numbers of messages that can be accessed from anywhere in the world via authenticated calls using HTTP or HTTPS.
* A queue can contain as many messages as your storage account has room for (potentially millions) and each individual message can be up to 64 KB in size.
* Queues are commonly used to create a backlog of work to process asynchronously and can be combined with compute functions like Azure Functions to take an action when a message is received.
* Disk storage, or Azure managed disks, are block-level storage volumes that are managed by Azure for use with Azure VMs.
* Conceptually, they’re the same as a physical disk, but they’re virtualized – offering greater resiliency and availability than a physical disk.
* With managed disks, all you have to do is provision the disk, and Azure will take care of the rest.

# Exercise - Create a storage blob #

### RETRY ###
* In this module, you will learn how to create a storage account and work with blob storage in Azure.
*Steps to create a new storage account:
Sign in to the Azure portal at https://portal.azure.com
Select Create a resource
Under Categories, select Storage
Under Storage Account, select Create
Fill in the required information such as subscription, resource group, storage account name, location, performance, and redundancy.
Once the storage account is created, you can work with blob storage by creating a container, uploading blobs (files) to the container, and changing the access level to allow anonymous read access for blobs.
Clean up: The sandbox automatically cleans up your resources when you're finished with this module. When you're working in your own subscription, it's a good idea to identify whether you still need the resources you created, as they can cost money. You can delete resources individually or delete the resource group to delete the entire set of resources.

# Identify Azure data migration options #

* Azure Migrate is a service that helps you migrate from an on-premises environment to the cloud.
* Azure Migrate functions as a hub to help you manage the assessment and migration of your on-premises datacenter to Azure.
* Azure Migrate provides a unified migration platform, a range of tools for assessment and migration, and integrated tools such as Azure Migrate: Discovery and assessment, Azure Migrate: Server Migration, Data Migration Assistant, Azure Database Migration Service, and Web App migration assistant.
* Azure Data Box is a physical migration service that helps transfer large amounts of data in a quick, inexpensive, and reliable way.
* Azure Data Box is a proprietary storage device with a maximum usable storage capacity of 80 terabytes.
* The Data Box is shipped to and from your datacenter via a regional carrier.
* Azure Data Box is ideal for transfer data sizes larger than 40 TBs in scenarios with no to limited network connectivity.
* Data Box can be used to import data to Azure and export data from Azure.
* Data Box can be used for one-time migration, moving a media library, migrating VM farms, SQL servers, and applications, moving historical data, initial bulk transfer, and periodic uploads.
* Data Box can also be used for disaster recovery, security requirements, and migrating back to on-premises or to another cloud service provider.
* Once the data is uploaded or exported, the disks on the device are wiped clean in accordance with NIST 800-88r1 standards.

# Identify Azure file movement options #

* AzCopy is a command-line utility for copying blobs or files to and from Azure storage accounts, and can also be configured to work with other cloud providers.
* Synchronizing files with AzCopy is one-directional, and does not synchronize bi-directionally based on timestamps or other metadata.
* Azure Storage Explorer is a standalone app that provides a graphical interface for managing files and blobs in Azure storage accounts, using AzCopy on the backend.
* Azure File Sync is a tool that allows for centralizing file shares in Azure Files, while maintaining the flexibility, performance, and compatibility of a Windows file server.
* Azure File Sync allows for using any protocol available on Windows Server to access data locally, including SMB, NFS, and FTPS.
* Azure File Sync allows for multiple caches across different locations, and also allows for replacing a failed local server by installing Azure File Sync on a new server in the same datacenter.
* Azure File Sync also allows for configuring cloud tiering, where frequently accessed files are replicated locally, while infrequently accessed files are kept in the cloud until requested.

# Knowledge Check #

1. Which tool automatically keeps files between an on-premises Windows server and an Azure cloud environment updated?
>Azure File Sync maintains a bidirectional synchronization of files between your on-premises and cloud Windows servers.

2. Which storage redundancy option provides the highest degree of durability, with 16 nines of durability?
>Geo-redundant storage (GRS) and geo-zone-redundant storage (GZRS) both provide 16 nines of durability.

3. Which Azure Storage service supports big data analytics, as well as handling text and binary data types?
>Azure Blobs is a massively scalable object store for text and binary data. Azure Blobs also includes support for big data analytics through Data Lake Storage Gen2.