# Demo - Azure Storage Introduction

This guide provides an introduction to some basic Azure Storage concepts.  In this demonstration you will show how to 
*	Create an Azure storage account using the Azure portal.
*	Describe the replication options such as LRS, ZRS and (RA-)GRS.
*	Show how and where Virtual Machine disks are persisted in an Azure Storage Account.
*	Demonstrate that within the virtual machine instance, the disks (VHDs) in the Azure Storage account look and feel just like a disk you’re used to working with in an on-premises or virtualized environment.
*	Explain the temporary storage on D: and point out that it doesn’t exist in your Azure storage account.
*	Show how to create a new simple volume.
*	Show how to create a new striped volume.

#### Pre-Requisites
This section lists the pre-requisites required for this demonstration.
*	Azure subscription

#### Setup
Estimated time: 15 minutes

1.  Open a browser and navigate to <https://github.com/Azure/azure-quickstart-templates/tree/master/101-vm-multiple-data-disk>. This is an ARM template that will deploy a VM with 4 data disks attached to the VM.
2.	Click the Deploy to Azure button.
3.	In the Custom deployment blade, click on Parameters.  Fill in the parameters as shown.  Note: you will need to come up with a unique name of your own for the storage account name and DNS name. For the VM Size use Standard_A2 and for the data disk size enter 1023.

<img src="./media/image001.jpg" align="center"/>

4.	Click on Resource group and create a new resource group.
5.	Click Legal Terms and accept the terms.
6.	Click the Create button.

<img src="./media/image002.jpg" align="center"/>

7.	RDP into the virtual machine. 
8.	Open a Command Prompt as an Administrator.
9.	Type the following commands to online the 4 data disks.
  1. `DISKPART <ENTER>`
  2. `LIST DISK <ENTER>`
This will list all the disks.  The 4 data disks should be disks 2 through 5.
  3. `SELECT DISK 2 <ENTER>`
  4. `ATTRIBUTE DISK CLEAR READONLY <ENTER>`
  5. `ONLINE DISK <ENTER>`
Repeat steps b through d for disk 3, 4, and 5.
10.	Download DiskSpd from <https://gallery.technet.microsoft.com/DiskSpd-a-robust-storage-6cd2f223>. This is one of the tools the Azure Storage team recommends using to perform storage benchmark tests. Alternatively, the tool is provided as part of the demo script folder.
11.	Unzip DiskSpd to C:\Temp\DiskSpd.


