# Active Directory (Home Lab)

## Step 1: Installing Active Directory

1. Open Server Manager on Windows Server VM
2. Click on Manage(Top Right) and Select Add Roles and Features
![AD Install](../docs/screenshots/active-directory-install-1.png)
3. In Server Roles, select AD Domain Services, Remote Access, and DNS
![AD Install](../docs/screenshots/active-directory-install-2.png)
4. Proceed with default setup and click install Active Directory
5. Before closing installation page, click "Promote this server to a domain controller"
![AD Install](../docs/screenshots/active-directory-install-3.png)
6. In Deployment Configuration, Click "Add a new forest" and enter a root domain name (ending with .local)
![AD Install](../docs/screenshots/active-directory-install-4.png)
7. In Domain Controller Options, create a DSRM password
![AD Install](../docs/screenshots/active-directory-install-5.png)
8. Proceed with default setup, click install and system will reboot 

## Step 2: Basic Active Directory Setup

1. Log in to Windows Server VM
2. Open Active Directory Users and Computers, navigate to domain file
![AD Setup](../docs/screenshots/basic-ad-setup.png)

## Step 3: Creating OU(Organizational Unit)

1. Right-click domain and select new -> organizational Unit
2. Type OU for department "USA" and click OK
3. Repeat Process for "Europe" and "Asia"
![OU Creation](../docs/screenshots/ou-creation.png)

4. Create different OU's(Computer,Users,Servers) within the OU departments
5. Repeat Process for "Europe" and "Asia"
![OU Creation](../docs/screenshots/ou-creation-2.png)

## Step 4: Creating Groups

1. Select a OU inside one of the OU Departments and select New -> Group
2. Type Group Name
2. Select Group Scope(Where the group can be used)
    - Domain Local(Only inside it's own domain)
    - Global(Inside it's domain and in any domain in the forest)
    - Universal(Across all domains in the forest)
3. Select Group Type(What group is used for)
    - Security(Control Permissions)
    - Distribution(Email Lists w/ no permissions)
4. Click OK
![Group Creation](../docs/screenshots/create-groups.png)
![Group Creation](../docs/screenshots/create-groups-2.png)
![Group Creation](../docs/screenshots/create-groups-3.png)

## Step 5: Creating Users

1. Select a OU inside one of the OU Departments and select New -> User
2. Fill in credentials of the new User and create password
3. Click Finish
![User Creation](../docs/screenshots/create-users.png)
![User Creation](../docs/screenshots/create-users-2.png)
![User Creation](../docs/screenshots/create-users-3.png)
