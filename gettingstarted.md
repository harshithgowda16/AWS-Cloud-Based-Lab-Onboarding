---
sidebar_position: 1
slug: /Admin/LabDeveloper/Guide For Onboarding Labs/Cloud Based Labs Onboarding/AWS  Based Lab Onboarding.md
---

# AWS Based Lab Onboarding
 
## Overview:
 
This document provides a comprehensive guide to the end-to-end process of onboarding an AWS based lab scenario using the CloudLabs portal. Within this document, you will learn how to create a CloudFormation template, a CloudLabs template, set up a CloudLabs On Demand Lab (ODL), manage users, and troubleshoot basic issues.

AWS based labs are effective when you want to provide a hands-on learning experience to your users or students on AWS Cloud. These labs are particularly useful for learning about AWS, like using AWS Identity and Access Management (IAM) for identity and access management to users, deploying resources such as S3 Buckets, EC2 Instances and many more. To set up a lab successfully, follow the instructions listed below.

In this document you will be going through with the below topics:

  - [Prerequisites](#prerequisites)
  
  - [Information to use to onboard a AWS based lab](#information-to-use-to-onboard-an-aws-lab)

  - [Setup Template from CloudLabs](#setup-template-from-cloudlabs)

  - [Setup ODL from CloudLabs](#setup-odl-from-cloudlabs)

  - [Activate the lab](#activate-the-lab)

  - [Common Issues & Resolutions](#common-issues-and-resolutions)

## Prerequisites

Before you begin onboarding an AWS based lab through CloudLabs, ensure you have the following prerequisites:

1. Admin access to [CloudLabs Admin Centre](https://admin.cloudlabs.ai/) (If access is unavailable, kindly reach out to your point of contact or [CloudLabs Support](../../GuideForOnboardingLabs/ContactSupport.md)).

2. An active subscription in CloudLabs Admin Portal. Refer [How to Onboard AWS Accounts to CloudLabs Portal](https://docs.cloudlabs.ai/LabDeveloper/OnboardingAWSAccountstoCloudLabs) document.

3. Lab Guide/Reference documents containing necessary instructions, often provided through GitHub which are in GitMarkdown format.


## Information to use to onboard an AWS lab

To onboard an AWS based lab to CloudLabs, use the below details:

- **Subscription Types**:  To onboard a AWS based lab, you should firstly determine what type of access the participants would require and post that you need to select the Subscription type from one of the types below that CloudLabs offers. It is highly recommended that you apply access and policy constraints for the chosen subscription type.
   
    - **Dedicated Subscription** : One of the AWS Organization Member account will be given to the one user.

    - **Dedicated Tenant**: When a access to the Organization root account is needed. 
   

Once you are ready to Onboard the labs on CloudLabs Admin Portal, you need to follow the instructions mentioned below:

*Let’s begin with the Onboarding Process*:

## Setup Template from CloudLabs

1. The first step in the onboarding process is to create an CFT template through CloudLabs 

2. You can follow the detailed guide mentioned here to login to the CloudLabs Admin Portal

   - [Access CloudLabs Admin Portal](https://admin.cloudlabs.ai/)

3. Follow the below mentioned guide to Add Template in CloudLabs.

   - [Add template in CloudLabs](https://docs.cloudlabs.ai/LabDeveloper/AddingAWSTemplate)

You have successfully onboarded the template into CloudLabs.


## Setup ODL from CloudLabs

1. Now, you need to create the ODL and map the template which you have created in the previous step to it. Also, the ODL must be created and managed only by the admins and not users.

   > **Note:** One template can be mapped with multiple ODLs.

2. To create ODL from CloudLabs Admin Portal follow instructions mentioned in the below guide: 

   - [Create ODL in CloudLabs](https://docs.cloudlabs.ai/LabDeveloper/CreatingODL)

You have successfully onboarded the On-Demand Lab (ODL) into CloudLabs.

> **Note:** 

> a) Once you have tested the lab configurations from the ODL you created, it is recommended to create another ODL for production labs.

> b) For information on how to invite users, manage users, extend lab duration and much more, refer [Manage Access](../../../OnboardingDocs/ManageOnDemandLab.md) documentation.


## Activate the lab

1. From the **On Demand Labs** Page _(1)_, choose your ODL _(2)_ and click on the Users icon _(3)_ to register into the environment. 

   ![](/img/OnboardingDocs/ondemandlab.png)

2. Click on **+ Add User** and enter your details, then click on **Submit**. 

   ![](/img/OnboardingDocs/adduser.png)

3. Now you have successfully registered yourself as a user. 

4. Within the **Users** page, you will find an instance registered under your name, indicated by its status being in the Approved state _(1)_. Proceed by clicking the **Launch** _(2)_ button.

   ![](/img/OnboardingDocs/Approved.png)

5. Now you will be navigated to a different browser tab where you will be able to view the page as shown in the screenshot below. On this page, click on the **Launch Lab** button.

   ![](/img/OnboardingDocs/launchlab.png)

6. Upon clicking the **Launch Lab** button, the deployment process will initiate, leading you to the screen illustrated in the provided screenshot below:

   ![](/img/OnboardingDocs/odl-launchlab.png)

7. After the instance is successfully deployed,On the CloudLabs environment page you will be able to see the login credentials like in below provided screenshot:  

   ![](/img/OnboardingDocs/Detailspage.png)

8. You can also activate the lab at bulk using Bit.ly URL by following the below steps.

9. From the **On Demand Labs** Page, choose your ODL _(1)_ and note down the ODL ID. Click on the Elipses icon _(2)_ and select **Activate Codes** _(3)_ to create an activation code. 

   ![](/img/OnboardingDocs/odl-select-odl.png)


10. Click on **+ ADD ACTIVATION CODE** 

   ![](/img/OnboardingDocs/odl-add-activation-code.png)

11. Provide the below values for the Activation Code properties.

   - **Name:** The Activation code should always follow the naming convention **ACTIVATE<**--**ODL-ID**--**>**. For instance, if your ODL ID is 1462, then the Activation Code will be **ACTIVATE1462**.

   - **Customer:** Provide your company/customer name.

   - **City:** Provide your city name.

   - **Country:** Select your country from the dropdown.

   - **Expiry Date:** Select an expiry date for the Activation code, post which the Activation code will be invalid.

Finally, click **Submit** to save details.

   ![](/img/OnboardingDocs/odl-provide-activation-code.png)

12. Copy the Bit.ly URL and share it with the users.

    ![](/img/OnboardingDocs/odl-copy-bitly-url.png)

13. Users can activate their labs by following the below steps:
     -	Navigate to the Bit.ly URL.
     -	Provide the required details.
     -	Click on Submit.

     ![](/img/OnboardingDocs/registrationpage.png)


## Common Issues and Resolutions

1.If you are creating files for IAM Policies and adding it in CloudLabs, make sure the URLs of files are publicly accessible.

2. Make sure you are adding the URLs of IAM Policy and UsagePolicy files in its respective fields.

3. While creating the ODL, make sure you map the ODL with correct template to avoid conflict in labs.

4. Ensure you are following the Syntax correctly while creating the IAM Policies to avoid deployment failures.
