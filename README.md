# RHEL 9 RAID + LVM + Apache Deployment
This project demonstrates a complete RHEL 9 infrastructure setup implementing RAID 5 for fault tolerance, LVM (PV–VG–LV) for storage management, Apache web server deployment on RAID-backed storage, SELinux configuration, and client-server validation.

## Project Overview
In this project, I built a complete RHEL 9 server setup focusing on storage redundancy and web server deployment. The server uses RAID 5 for fault tolerance and LVM for flexible storage management. Apache is configured to serve content from RAID-backed storage with proper SELinux and firewall configuration.
The goal was to simulate a production-style Linux infrastructure environment.

## Environment
- RHEL 9 (Server)
- VMware (Lab setup)
- 3 Virtual disks for RAID 5
- 1 Client machine for testing

## Architecture Design
- Three disks combined into a RAID 5 array using mdadm
- RAID device used as a Physical Volume (PV)
- Created Volume Group (VG) on RAID storage
- Created Logical Volume (LV) for web data
- Formatted and mounted LV to /var/www/html
- Installed and configured Apache (httpd)
- Adjusted SELinux context for web directory
- Configured firewalld to allow HTTP traffic
- Verified web access from client system

## Validation Commands Used
- lsblk
- cat /proc/mdstat
- pvs, vgs, lvs
- systemctl status httpd

## Skills Demonstrated
- Linux System Administration
- RAID 5 Configuration (mdadm)
- LVM Storage Management
- Apache Web Server Deployment
- SELinux Configuration
- Firewall Configuration
- Persistent Storage Setupbut 

## Future Improvements
- SSL (HTTPS)
- Log monitoring
- Disk failure simulation
- Backup strategy
  
