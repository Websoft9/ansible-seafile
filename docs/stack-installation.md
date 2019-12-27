# Initial Installation

If you have completed the Seafile deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:80 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Seafile

## Seafile Installation Wizard

1. Using local Chrome or Firefox to visit the URL *http://domain name* or *http://Internet IP*, you will log in interface of Seafile
   ![Seafile login](https://libs.websoft9.com/Websoft9/DocsPicture/en/awx/awx-login-websoft9.png)

2. The Adminitrator console of Seafile... 
   ![Start Seafile](https://libs.websoft9.com/Websoft9/DocsPicture/en/awx/awxui-websoft9.png)

3. Then start to create: Credentials, Inventories, Project for one Template, use the Template for deployment job

> More useful Seafile guide, please refer to [Ansible Tower Documentation](https://docs.ansible.com/ansible-tower/)

## Q&A

#### I can't visit the start page of Seafile?

Your TCP:80 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### Which database does this Seafile use?

PostgreSQL

#### The first time loading is slow?

Yes, Seafile takes nearly a minute to load and runs smoothly after loading
