Sort Azure Active Directory App Registrations by status
=======================================================

            

**DESCRIPTION**


This PowerShell Runbook (compatible with PowerShell Core) connects to Azure and Azure Active Directory using an Automation Run As account, retrieves all app registrations within the tenant and sort them as Active (if credentials have not expired yet) or
 Expired (if credentials have already expired). The output is displayed within the output stream and in a CSV file stored in container within a storage account which will be created for this purpose. You can attach a recurring schedule to this runbook to run
 it at a specific time.


**REQUIRED**


1. An Automation connection asset called AzureRunAsConnection that contains the information for connecting with Azure using a service principal and Application Administrator right on the tenant to list all App Registrations. To use an asset with a different
 name you can pass the asset name as a input parameter to this runbook.


2. A storage account name that follows your naming convention and Azure naming restrictions.


3. A container (part of the specified storage account) name that follows your naming convention and Azure naming restrictions.


4. The name of the location that will host the storage account.


3. The name of the resource group that will host the storage account.


4. All the following PowerShell modules are required to run the cmdlets : Az.Accounts, Az.Storage, AzureAD and Az.Automation.


**AUTHOR**


Farouk FRIHA


**LAST EDIT**


2019-05-08


**RELEASE NOTES**


2019-05-08 First release


**RUNBOOK CONTENT**


** **

 

 
**

** **


** **

** 
**

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
