# Username and Password

These accounts are required for Seafile image installation and configuration

## Seafile

Administrator account is set by yourselft at the time of Seafile installation wizard

## PostgreSQL

* Administrator username: *`potgres`*
* Administrator password: stored in the file of your server instance: */credentials/password.txt*. You use the **online SSH interface on Cloud Console** and run the command `cat /credentials/password.txt` to get the database password
   ![Run the cat command](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpasswordps-websoft9.png)

> If you want to log in MySQL, refer to [PostgreSQL Web interface Management](/admin-postgresql.md)

## Linux

* Host Name: Internet IP or Public IP of your Instance
* Connect by: Online SSH on Cloud Console or SFTP/SSH tools on your local computer
* Password: It was set by yourself when created instance
* Username: Different Cloud Platform has differences
   |  Cloud Platform   |  Administrator Username   |
   | --- | --- |
   |  Azure   |  It was set by yourself when created instance   |
   |  AWS   |  ubuntu   |
   |  Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud |  root   |

If don't remember the password of Linux, you should reset password on Cloud Console