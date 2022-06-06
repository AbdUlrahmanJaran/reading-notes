# Azure Blob storage
Azure Blob storage is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data. Unstructured data is data that doesn't adhere to a particular data model or definition, such as text or binary data.

### Blob storage is designed for:
- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Writing to log files.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.

### Blob storage offers three types of resources:
1. The storage account
2. A container in the storage account
3. A blob in a container

A container organizes a set of blobs, similar to a directory in a file system. A storage account can include an unlimited number of containers, and a container can store an unlimited number of blobs.

``AzCopy``, ``Azure Data Factory`` and ``Azure Import/Export service`` are used to Move data to Blob storage.

## Things I want to know more about
1. Azure Storage Data Movement library.
2. Storage accounts.

### Ref: (Microsoft Blob storage Intro)[https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction]