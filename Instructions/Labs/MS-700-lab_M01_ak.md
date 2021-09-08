---
lab:
    title: 'Lab 01: Manage roles and create teams'
    type: 'Answer Key'
    module: 'Module 1: Microsoft Teams in Microsoft 365'
---

# **Lab 01: Managing Microsoft Teams**

## **Microsoft 365 user interface**

Given the dynamic nature of Microsoft cloud tools, you may experience user interface (UI) changes that were made following the development of this training content. This will manifest itself in UI changes that do not match up with the detailed instructions presented in this lab manual.

The Microsoft World-Wide Learning team will update this training course as soon as any such changes are brought to our attention. However, given the dynamic nature of cloud updates, you may run into UI changes before this training content is updated. **If this occurs, you will have to adapt to the changes and work through them in the lab exercises as needed.**

## **Lab Scenario**

In the labs, of this course, you will assume the role of **Joni Sherman**, a Teams Administrator for Contoso Ltd. and her pilot team that shall evaluate the capabilities of Microsoft Teams in a testing environment. You have implemented Microsoft 365 in a virtualized lab environment already and were commissioned to conduct a pilot project to test the implementation of Microsoft Teams against Contoso Ltd. business requirements.

You have just started the pilot project, and you’ve already got two virtual machines with preinstalled Teams Desktop clients and a tenant with different users:

- Joni Sherman (JoniS@&lt;YourTenant&gt;.OnMicrosoft.com) **Group coordinator / Teams admin**

- Alex Wilber (AlexW@&lt;YourTenant&gt;.OnMicrosoft.com) **Regular pilot user from Canada**

- Lynne Robbins (LynneR@&lt;YourTenant&gt;.OnMicrosoft.com) **Regular pilot user**

- Allan Deyoung (AllanD@&lt;YourTenant&gt;.OnMicrosoft.com) **Teams communication support engineer**

- Megan Bowen (MeganB@&lt;YourTenant&gt;.OnMicrosoft.com) **Regular employee**

## **Objectives**

After you complete this lab, you will be able to:

- Assign Teams admin roles to users

- Check license assignment for users

- Understand the Teams admin center and it’s menus

- Install the Teams PowerShell module and explore its cmdlets

- Create Microsoft 365 Groups from the M365 admin center

- Create new teams using the Teams Desktop client

- Create new teams using the Teams web client

## **Lab Setup**

- **Estimated Time:** 60 minutes.

## **Instructions**

### **Before you start**

The lab in this course have been prepared for a Microsoft Teams deployment at Contoso Ltd. Corporation. Contoso is running a Microsoft 365 cloud only deployment. The lab environments have been specifically designed in this manner to give you experience managing Microsoft Teams in a Microsoft 365 deployment. You will be provided with two virtual machines and a Microsoft 365 tenant to complete the lab steps.

```
Note : 
Please note that odl_userXXXXX@<YourTenant>.onmicrosoft.com is your administrator user and you should use odl_userXXXXX@<YourTenant>.onmicrosoft.com in place of MOD Administrator (admin@<YourTenant>.onmicrosoft.com) throughout this lab
```
  
#### **1. Sign in to the lab virtual machines**

The labs in this course will use two virtual machines:

- Client 1 VM : a stand-alone Windows 10 client virtual machine with Microsoft Teams pre-installed.

- Client 2 VM : a stand-alone Windows 10 client virtual machine with Microsoft Teams pre-installed.

**Note:** Lab virtual machine sign in instructions will be provided to you by your instructor.

**Important:** The exercises in the MS-700 labs are cloud-only deployments. A local administrator account has been created on the client VMs. You will log into the VMs as a local administrator instead of a domain account. Following your login, the desktop will indicate that you are logged in as either **CLIENT1\Admin** or **CLIENT2\admin**, depending on which machine you are on.

#### **2. Review installed applications**

Once you signed in to the VM, observe the start menu, and verify following applications have been installed:

- Microsoft Teams

#### **3. Review Microsoft 365 tenant**

Beside two VMs, you will also be provided with a Microsoft 365 tenant with following highlights:

- Office 365 E5 with Enterprise Mobility + Security E5 licenses assigned to various users

- One Global Administrator (MOD Administrator) and 9 standard users have been pre-created.

  **Note:** Microsoft 365 sign in instructions will be provided to you by your instructor.

- The username of the Global Administrator (MOD Administrator) is **admin@&lt;YourTenant&gt;.onmicrosoft.com**.

```
Note : 
Please note that odl_userXXXXX@<YourTenant>.onmicrosoft.com is your administrator user and you should use odl_userXXXXX@<YourTenant>.onmicrosoft.com in place of MOD Administrator (admin@<YourTenant>.onmicrosoft.com) throughout this lab
```

- **&lt;YourTenant&gt;.onmicrosoft.com** - This is the domain associated with the Microsoft 365 tenant that was provided by the lab hosting provider. The first part of this domain name (&lt;YourTenant&gt;) is the unique tenant ID provided by the lab hosting provider. The &lt;YourTenant&gt; portion of the tenant ID, which is the tenant suffix ID, will be unique for each student.

  **IMPORTANT:** This is critical because throughout this lab, you will be asked to enter the **&lt;YourTenant&gt;.onmicrosoft.com** domain name when signing into apps with a given username (for example, JoniS@&lt;YourTenant&gt;.onmicrosoft.com). When doing so, you must enter the unique tenant suffix ID that is assigned to your tenant ID in place of the **&lt;YourTenant&gt;**.

  For example, if your Tenant Email is **admin@contosolab.onmicrosoft.com**, the unique tenant suffix ID (&lt;YourTenant&gt;) is **contosolab**. When signing in as Joni when entering this domain, you would replace &lt;YourTenant&gt; with contosolab (for example, JoniS@contosolab.onmicrosoft.com).

   **RECOMMENDATION:** You should write down your unique tenant suffix, mentioned as &lt;YourTenant&gt; in this lab and provided by your training provider. After a while, you will have this name or number memorized as you move through the labs in this course.

- **Use the new Microsoft 365 admin center** 

  Throughout the lab exercises for this course, if you navigate to the Microsoft 365 admin center, make sure the slider in the upper right corner is set to **The new admin center**. If you can read **Try the new admin center**, select the slider and activate it.  
‎‎  
‎‎  **IMPORTANT:** The instructions that are provided in the lab exercises for this course are based on the new Microsoft 365 admin center UI and not the classic UI.

### **Exercise 1: Prepare team roles and licenses**

In the first exercise you will assign required administrative roles to users, check license assignments for the Teams license and then explore the Microsoft Teams admin center. To perform these tasks, you will use default tenant global admin and the Joni Sherman’s account (JoniS@_&lt;YourTenant&gt;_.onmicrosoft.com).

#### **Task 1 - Assign Teams admin roles to users**

In this task you will use the default global admin to sign in to the Microsoft 365 admin center and assign several Teams admin roles to different users. This task is crucial for later tasks and exercises as you will perform most of the tasks in context of Joni Sherman’s account.

1. Browse to Microsoft 365 admin center (https://admin.microsoft.com/) as **MOD Administrator**. 

    1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

    2. Open **Microsoft Edge** and browse to the **Microsoft 365 admin center** at [**https://admin.microsoft.com/**](https://admin.microsoft.com/) with the Global admin credential ( **MOD Administrator** : admin@&lt;YourTenant&gt;.onmicrosoft.com) .

2. Assign **Teams admin** role to **Joni Sherman**

    1. Select the navigation menu in the upper-left and select **Users** and **Active users** from below it.

    2. In the Active users list, search and select **Joni Sherman**, to open the right-side settings pane.

    3. In the settings below the Account tab, scroll to **Roles** and select **Manage roles** below.

    4. On the **Manage admin roles** pane, select **Admin center access** and scroll down to select **Show all by category** to reveal all avaliable roles. 
    
    5. Select **Teams Administrator** checkbox then select **Save changes**. You will see the message **Admin roles updated** on the upper part of the pane to comfirm the update. 

3. Assign **Teams device admin** role to **Alex Wilber**

    Repeat the same steps and assign **Teams Device Administrator** role to **Alex Wilber**.

4. Assign **Teams communication admin** role to **Allan Deyoung**

    Repeat the same steps and assign **Teams communication admin** role to **Allan Deyoung**.

You have now successfully assigned the Teams admin roles.

* Teams Administrator: Joni Sherman
* Teams Devices Administrator: Alex Wilber
* Teams communication admin: Allan Deyoung 

Proceed to the next task.

#### **Task 2 – Check license assignment of your users**

In this task, you will check the license assignment of all users participating in the pilot. At the end of the task you will confirm that all pilot users are licensed correctly and Alex Wilber’s location is updated to Canada as preparation for a later task.

1. Connect to the **Client 1 VM** and browse to Microsoft 365 admin center (https://admin.microsoft.com/) as **MOD Administrator**.

2. Update **Alex Wilber's** location to **Canada**

    1. On the **Users** > **Active users** page, select the name of **Alex Wilber**.

    2. Select **Licenses and Apps** tab. 

    3. Select the dropdown menu under **Select location**, and update to **Canada**. 

    4. Select **Save changes**. 

3. Check **Alex Wilber's** licenses

    1. On the same tab, under **Licenses** section, verify that **Enterprise Mobility + Security E5** and **Office 365 E5** are both selected.

    2. Select **Apps** to expand All licenses.

    3. Scroll down the list of all apps, and verify **Microsoft Teams** is selected. 
    
4. You can repeat the same steps to check other users' licenses. Do not change their locations. 

You have successfully validated that all users participating in the pilot own Teams licenses and are ready to start working with Teams. You have also changed the location of Alex Wilber to Canada, as a preparation for a later task. Continue with the next task. 

You have finished the first exercise, and you can continue with the next one.

### **Exercise 2: Explore Teams management tools**

In this exercise you will install the Teams PowerShell module, required to manage teams, policy packages, calling features, and all other settings for Teams in your tenant. You can perform most of the tasks possible from the Teams admin center also in the PowerShell. You can create scripts for automation and even access several settings not available in the GUI.

#### **Task 1 - Explore Teams admin center**

You will review the available settings for managing Teams in the Teams admin center.

1. Connect to the **Client 1 VM** and browse to Teams admin center (https://admin.teams.microsoft.com) as **Joni Sherman**  (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).

    **Note:** You can use **InPrivate window** of Microsoft Edge for logging in with different credentials. 

2. In left navigation of the Teams admin center, select **Teams** > **Manage teams**.

3. The **Manage teams** page show the existing teams in your organization. Note that there is an org-wide team named **Contoso** that is automatically created for new tenant with less than 5000 users.

4. In left navigation of the Teams admin center, select **Teams** > **Teams policies**. You can see the default Teams policy named **Global (Org-wide default)**.

You can explore other settings to familiarize various controls in the Teams admin center.

You have successfully explored several available menus from the Teams admin center for managing teams and configuring policies in your tenant. 

#### **Task 2 - Install and explore Teams PowerShell module**

In this task, you will install and connect with the Teams PowerShell module to your tenant and explore the available cmdlets and functions to manage your tenant. You can install the Teams PowerShell module from the available repositories preconfigured in your Windows 10 operating system and do not need to download any executables via the browser.

1. Connect to the **Client 1 VM** with the VM credential that have been provided to you.

2. Open **Windows PowerShell** and run as Administrator.

    1. Select **Start** and search for **Windows PowerShell (Admin)**, then right select **Run as administrator**.

    2. Confirm the **User Account Control** window with **Yes**.

3. Install **Microsoft Teams PowerShell module**

    1. In the PowerShell window, enter the following cmdlet and press **Enter:**

        ```powershell
        Install-Module -Name MicrosoftTeams
        ```
    2. Enter **Y** and press **Enter** twice to confirm the installation of the NuGet provider and Untrusted repository.

4. Connect to your tenant.

    1. Enter the following cmdlet in the PowerShell window and press **Enter**:

        ```powershell
        Connect-MicrosoftTeams
        ```
    2. In the Sign in window, sign in as Teams admin - Joni Sherman (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).

        When the sign in was successful, several information about the signed in user and the tenant are displayed. 
        
5. Explore **Microsoft Teams PowerShell module**

    1. To confirm the MicrosoftTeams module is loaded correctly, enter the following cmdlet and press **Enter** to view all available PowerShell modules:

        ```powershell
        Get-Module
        ```
        **Note**: To the left of the **Name** column, the version of the PowerShell module is displayed.

    2. To get an overview of the available Teams PowerShell cmdlets from the MicrosoftTeams module, enter the following cmdlet and then press **Enter**:

        ```powershell
        Get-Command -Module MicrosoftTeams
        ```

    3. The Get-Help cmdlet is used explore the available cmdlets. For example, to get more information about how to create a team with PowerShell, enter the following cmdlet and press **Enter**:

        ```powershell
        Get-Help New-Team
        ```

        If you receive a message to update the help libraries, type **Y** for yes.

    4. Disconnect from the Microsoft Teams environment.  

        ```powershell
        Disconnect-MicrosoftTeams
        ```
6. Close the PowerShell window and continue to the next task.

You have successfully used the Microsoft Teams PowerShell module to connect to Teams and explored available cmdlets.

### **Exercise 3: Create groups and teams**

In this exercise, you will create some resources required in later tasks. These include creating a Microsoft 365 Group from the Microsoft 365 admin center and creating a team in the Desktop client and then the web client.

#### **Task 1 - Create a Microsoft 365 Group**

You will create a new Microsoft 365 Group named "IT-Department," and then add the pilot members serving as a basis for your future teams and licensing.

1. Connect to the **Client 1 VM** and browse to the **Microsoft 365 admin center** (https://admin.microsoft.com/) as **Joni Sherman**  (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).

2. In the Microsoft 365 admin center, select **Groups** > **Active** **Groups**.

3. On the **Active groups** page, select **Add a group**.

4. Follow the **Add a group** wizard with the following information:

    * Group type : Select **Microsoft 365 (recommended)**.
    * Basics : 
    	- Name: **IT-Department**
    	- Description: **All staff of the IT-Department**
    
    * Owners : 
        - Select **+ Assign owners** 
        - Search and select **Joni Sherman**
        - Select **Add(1)**, and then select **Next**.

    * Members : 
        - Alex Wilber
        - Allan Deyoung
        - Lynne Robbins
        - Megan Bowen

    * Settings : 
        - Enter **IT-Department** for Group email address. 
        - Privacy : Private
        - Uncheck **Create a team for this group**.

5. Select **Create group** > **Close**.

6. Wait a moment and select **Refresh** until the group is visible. You will see there is no Teams icon in the **Teams status** column.

7. Select the **IT-Department** group to review the settings and members. 

The new Microsoft 365 Group with the name "IT-Department" was successfully created. Close the browser window and continue to the next task.

#### **Task 2 - Create a new team by using the desktop client**

To test the self-service capabilities of Teams, in this task, **Megan Bowen** will sign in to the Teams Desktop client, create a new team with the name **Teams Rollout** and add all members participating in the Teams evaluation project.

1. Connect to the **Client 2 VM** with the credentials that have been provided to you.

2. Select the **Teams** icon on the taskbar to start the Teams Desktop client.

3. When prompted to **Enter your work, school or Microsoft account**. Sign in as **Megan Bowen** (MeganB@&lt;YourTenant&gt;.onmicrosoft.com).

4. In the Teams client, select **Join or create a team** from the lower left corner. 

5. Select **Create team** >**From scratch** > **Public**. Enter the team name **Teams Rollout** and select **Create**.

6. On the **Add members to Teams Rollout** window, enter the following names and select **Add**. 

    * Alex Wilber
    * Allan Deyoung
    * Joni Sherman
    * Lynne Robbins

7. Select the dropdown menu next to Joni Sherman and switch from **Member** to **Owner**. 

8. Select **Close**.

You have successfully created a new team from the Teams desktop client, added the project team members, and you have made Joni Sherman a team owner. 

#### **Task 3 - Create a new team by using the web client**

In this task, **Lynne Robbins** will continue testing the self-service capabilities of Teams by using the Teams web client to create another team with the name **Sales**. She will also add Megan Bowen as a member.

1. Connect to the **Client 2 VM** with the credentials that have been provided to you.

2. Browse to the **Microsoft Teams web client** at [**https://teams.microsoft.com**](https://teams.microsoft.com/) and sign in as **Lynne Robbins** (LynneR@&lt;YourTenant&gt;.onmicrosoft.com).

4. Select **Join or create a team** from the lower left corner. 

5. Select **Create team** >**From scratch** > **Private**. Enter the team name **Sales** and select **Create**.

6. On the **Add members to Sales** window, enter the following names and select **Add** > **Close**.

    * Megan Bowen

You have successfully created a new team with the Teams web client. This is the end of lab 1. You can close all browser windows and proceed to the next lab.

END OF LAB
