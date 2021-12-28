# Prepare and configure your SAP Cloud Platform environment 

## Introduction

You will now prepare your SAP Cloud Platform Account, configure your entitlements and configure your account for our extension scenario.

**Persona:** SCP Developer

### Prepare your SAP Cloud Platform Account

1.	Open your *SAP Cloud Platform Cockpit*
2.	Navigate to your *Global Account-> Subaccounts*
3.	Press button to create a *New Subaccount*
   ![Create Subaccount](./images/Prepare-Cloud-Platform-1.png)

4.	Configure your Subaccount in the pop-up: 
       - *Display Name:* Choose a name 
       - *Provider:* AWS, 
       - *Region:* Europe (Frankfurt), 
       - *Subdomain:* Choose a subdomain
       - Select 'Enable Beta Features' 
5.	Click on *Create*

   ![Configure Subaccount](./images/Prepare-Cloud-Platform-2.png)
   
6.	Once your account is created, select your *Subaccount*
7.	Choose *Enable Cloud Foundry*

   ![Enable CF](./images/Prepare-Cloud-Platform-3.png)
 
8.	Fill out *Organization Name* and click on *create*

   ![Organization Name](./images/Prepare-Cloud-Platform-4.png)
   
9.	Select *Members* in the menu on the left and then click on *Add Members*

   ![Add Member](./images/Prepare-Cloud-Platform-5.png)
   
   Hint: There might be an alternative route to add users. Go to *Org Members* on the left in case that your menu structure looks different and then follow the steps below.
   
10.	Add Users to the Space by adding their IDs in the text field. *Assign Roles* as Organization Manager. Click on *OK*

   ![Assign role](./images/Prepare-Cloud-Platform-6.png)
   
11.	Switch to the *Spaces* tab and click on *Create Space*

   ![Create Space](./images/Prepare-Cloud-Platform-7.png)
   
12.	Select *Space Name* 'BusinessPartner' in the pop up and make sure you assign the roles 'Space Manager' and 'Space Developer' and click on *Create*

   ![Configure Space](./images/Prepare-Cloud-Platform-8.png)
   
13.	Click on your created Space 'Business Partner'

   ![Click Space](./images/Prepare-Cloud-Platform-9.png)
   
14.	Then switch to *Members* in the menu on the left, and choose *Add Members*
   
15.	Add Users to the Space by adding their IDs in the text field. *Assign Roles* as Space Developer. Click on *OK*

      ![Add Member](./images/Prepare-Cloud-Platform-10.png)
   
16.	Switch to the *Security* tab -> *Administrator*, then choose *Add Administrator*

   ![Add user](./images/Prepare-Cloud-Platform-11.png)
   
17.	Add Users to the Space by adding their IDs in the text field and click on *OK*

 ![Add Admin](./images/Prepare-Cloud-Platform-12.png)

### Configure Entitlements

1.	Navigate to your *Entitlements -> Configure Entitlements*

  ![Add users](./images/Prepare-Cloud-Platform-13.png)
   
2.	Then choose *Add Service Plans*

   ![Entitlement](./images/Prepare-Cloud-Platform-14.png)
   
3.	Search for 'Enterprise Messaging', then click on *Enterprise Messaging*

   ![Add Service Plans](./images/Prepare-Cloud-Platform-15.png)

4.	Select *Available Service Plans* -> 'default'

5.	Do the same for the following services:
       - '*Extension Factory Serverless runtime*' -> Select Available Service Plans -> 'default'
       - '*SAP HANA Schemas & HDI container*' ->Select Available Plans -> "hdi-shared"
       - '*SAP HANA service*' -> Select Available Service Plans -> "64STANDARD"
       - '*Application Runtime*' -> Select Available Service Plans -> "MEMORY"
6.	Click on Add 5 Service Plans and save

### Configure your account

In this scenario differed applications are needed. To use these services, you first need to subscribe to them:

1.	Navigate to your *Subaccount -> Subscriptions*
   
2.	Search for 'Continuous Integration & Delivery'

![Add Service Plansa](./images/Prepare-Cloud-Platform-17.png)

  ![Search CI/CD](./images/Prepare-Cloud-Platform-18.png)
   
3.	Click on *Subscribe*

  ![Search CI/CD](./images/Prepare-Cloud-Platform-18.png)

4.	Repeat step 2&3 for 'Enterprise Messaging', 'Business Application Studio' and 'Extension Center' to subscribe to all needed applications.

### Set up roles

1.	Navigate to your *Subaccount -> Security*

2.	Choose *Role Collections* 

 ![Subscribe CICID](./images/Prepare-Cloud-Platform-19.png)
  
3.	Create a *new Role Collection*:
        Name:'Serverless_RoleCollection'
        Description: ''
     
 ![Role Collection](./images/Prepare-Cloud-Platform-20.png)
     
4.	Click on the name of your new role collection and choose *Add Role*
       - *Application Identifier:* select 'xfsrt-application'	
       - *Role Template:* 'Functionsmanage'	
       - *Role:* 'FunctionsManage'
     
 ![Create Role Collection](./images/Prepare-Cloud-Platform-21.png)
     
 
5.	Click on *Save*

6. Similarly add ODPManage, ODPAPIAccess roles to Serverless_RoleCollection

7.	Navigate Back to your *Subaccount* -> *Trust Configuration* and choose *SAP ID Service*

8.	Insert your E-Mail in the according field and click on *Show Assignments*

 ![Assign Role Collection](./images/Prepare-Cloud-Platform-27.png) 
 
9.	Click on *Assign Role Collection* then select  'Business_Application_Studio_Developer',

 ![Show Assignments](./images/Prepare-Cloud-Platform-26.png) 
 
10.	Repeat Step 8 for the following role collections: 'Serverless_RoleCollection' 
'CICD Service Administrator' and 'EnterpriseMessagingAdmininistrator'



