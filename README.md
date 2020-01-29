![MIKES DATA WORK GIT REPO](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_01.png "Mikes Data Work")        

# Adding Drive Space – Extending Disks From OS aka Spanned Volumes on SQL Server Datacenter Server in AWS
By mikesdatawork on December 2, 2014**        



## Contents    
- [About Process](##About-Process)  
- [SQL Logic](#SQL-Logic)  
- [Build Info](#Build-Info)  
- [Author](#Author)  
- [License](#License)       

## About-Process

<p>We used this method after the space was added via AWS. Once a drive was added to the OS, we first Initialized the Disk, and while the disk was still 'unallocated'; go to the drive you want to expand, and right-click and select 'Extend Volume'. We did this on the SQL Server Database Server Configured with AlwaysOn Failover Cluster within AWS. Server Version: Server 2008 R2 Datacenter – Windows 6.1.7601 Service Pack 1 Build 7601. Drives were added, and expanded on both nodes (INTE-SQLA-01 & INTE-SQLA-02) This was a safe no-risk operation, and did not cause any downtime for Services, or Databases. Below are the steps performed during this process. The drive we wish to extend is the SQL Log Drive ( Drive L: ). First thing you do is right-click the left pane of the new disk and select 'Initialize Drive'. The following steps show this process. Go to Start à Run, and type in 'diskmgmt.msc'. Once the new disk has been added, simply right-click and select 'Initialize'.<p>

![Drive Extension]( https://mikesdatawork.files.wordpress.com/2014/12/image002.jpg "New Disk Add")
 

Click 'OK'

![Initialize Disk]( https://mikesdatawork.files.wordpress.com/2014/12/image006.jpg "Click Ok")
On the following prompt keep the default settings, and Click 'OK'.  

![See Unallocated]( https://mikesdatawork.files.wordpress.com/2014/12/image008.jpg "See Disk Online")
Once it's completed it will simply display as 'Online', and remain in an 'Unallocated' state.  

![Extend Drive Volume]( https://mikesdatawork.files.wordpress.com/2014/12/image012.jpg "Extend Volume")
Go back to the original Drive you wish to extend ( Drive L: ) and right-click. Select 'Extend Volume'.  
Click 'Next' on the following prompt.

![Extend Volume Wizard]( https://mikesdatawork.files.wordpress.com/2014/12/image014.jpg "Extend Volume Wizard")
 
Select the disk on the left, and click 'Add', then 'Next'.

![Select Disk]( https://mikesdatawork.files.wordpress.com/2014/12/image018.jpg "Add Selected Disk")
 
Click 'Finish' and you're done.

![Extend Volume Complete]( https://mikesdatawork.files.wordpress.com/2014/12/image019.jpg "Click Finish")
 
The new disks are now 'Spanned Volumes' and will be represented in Purple under Disk Management.  When viewed from Windows Explorer; you will see the drive as 250GB.

![See Expanded Disk Volume]( https://mikesdatawork.files.wordpress.com/2014/12/image020.jpg "See Expanded Disks")
 




[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

[![Gist](https://img.shields.io/badge/Gist-MikesDataWork-<COLOR>.svg)](https://gist.github.com/mikesdatawork)
[![Twitter](https://img.shields.io/badge/Twitter-MikesDataWork-<COLOR>.svg)](https://twitter.com/mikesdatawork)
[![Wordpress](https://img.shields.io/badge/Wordpress-MikesDataWork-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)
 
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Mikes Data Work](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_02.png "Mikes Data Work")

