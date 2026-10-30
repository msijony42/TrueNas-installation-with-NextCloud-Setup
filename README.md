A Hardware/VM need.
2-4 cores, 4-8 GB RAM, and at least 1 disk for OS installation and at least 2 additional disks for RAID configuration.
Download TrueNAS SCALE OS and make it bootable.
Install TrueNAS on 1 Single disk (SSD recommended).
After installation, configure a password and the network for the NAS to access it from a web browser.
Username: truenas_admin, Pass: as you set.
After successful login, make sure your date & time are accurate.
Go to Storage>> Disk, create a RAID with selected disks. Mirror/Stripe as your need.
Now create a pool as needed (You can create multiple pools for multiple purposes, but Nextcloud needs a dedicated pool to run smoothly).
Once the pool is created, goto Datasets>>Your_Raid_Disk. create 3 Folder (AppData, Postgres, UserData)
Application File will install in AppData, the database will install in Postgres, all Stored Data will be in UserData Files.
Now, go to Apps>> Discover>> NextCloud.
During configuration of the Nextcloud installation. Timezone, PortNumber, Data pointing to specific folders, and auto permission must be done properly.
when installation done and try to access Nextcloud via browser, valid domain is required message show.
Now enable SSH service in the TrueNAS and access truenas via ssh.
cd /mnt/YOUR_RAID_DISK/Nextcloud/AppData/

# TrueNas-installation-with-NextCloud-Setup
In this repo TrueNas &amp; NextCloud will work, Raid System and Everything will show.
