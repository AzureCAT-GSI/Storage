# Understanding Azure Storage and Solution Performance
The Azure Storage system is a foundational building block for many services in the Azure Platform.  It has a touch point of about 85% of the services in the platform, meaning it's durability and scalability is proven. How is massive scalability achieved in this system?  Why do you care as a Solution Architect? What are some best practices for architecting your solutions so that durability and scalability are achieved?  These questions are addressed in this session.  You will learn internals of how the Azure Storage system works across all storage abstractions. As you progress through the session you will be introduced to capacity and constraints of the system. Lastly, you will learn some best practices on how to apply this knowledge in your architectures to deliver scalable and durable storage solutions.

##Presentation
Download the [PowerPoint](./Architecting%20Azure%20Storage.pptx?raw=1).
The PowerPoint includes full speaker notes helping you understand the slides, and everything you need to deliver the session.

## Demos
* Storage Introduction [Demo script](./Demo%201%20-%20Storage%20Introduction/Readme.md)
* Storage FileShare [Demo script](./Demo%202%20-%20Storage%20FileShare/Readme.md)
* Storage Disk IOPS [Demo script](./Demo%203%20-%20Storage%20Disk%20IOPS/Readme.md)

## Session objectives
Discuss Azure storage fundamentals and the importance of Storage choices
* Understand Storage Replication (LRS --> RA-GRS)
* Compare Standard Storage vs. Premium Storage
* Overview of Azure Storage subsystem architecture
* Discuss Storage Security (Access Keys/SAS, Encryption)
* Guidance and Best Practices

## Session Prerequisites
* An Azure Subscription

## Azure Services Covered
* [Azure Storage, Blobs, Files, Queues, Tables, Disks](https://azure.microsoft.com/en-us/documentation/services/storage/)
* [Standard Storage and limits](https://azure.microsoft.com/en-us/documentation/articles/storage-scalability-targets/)
* [Premium Storage](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage/)


## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or 
