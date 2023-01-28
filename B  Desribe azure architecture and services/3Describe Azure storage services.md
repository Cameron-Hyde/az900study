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