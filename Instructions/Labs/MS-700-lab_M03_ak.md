---
lab:
    title: 'Lab 03: Plan and configure network settings for Microsoft Teams '
    type: 'Answer Key'
    module: 'Module 3: Prepare the environment for a Microsoft Teams deployment'
---

# **Lab 03: Plan and configure network settings for Microsoft Teams**

## **Use the new Microsoft 365 admin center**

Throughout the lab exercises for this course, if you navigate to the Microsoft 365 admin center and are prompted with a window asking if you want to try the new Microsoft 365 admin center, always select the **Try it now** button.  
‎‎  
‎**‎IMPORTANT**: The instructions that are provided in the lab exercises for this course are based on the new Microsoft 365 admin center UI and not the classic UI.

## **Lab Scenario**

In the labs of this course you will assume the role of Joni Sherman, a Teams Administrator for Contoso Ltd. Your organization is planning to deploy Microsoft Teams. However, there are concerns about current network infrastructure to meet the requirements for Microsoft Teams services. Therefore, you need to analyze the current network infrastructure and perform bandwidth calculations. Based on your estimation, you can provide recommendations to the networking team. Furthermore, your organization is planning to purchase and deploy multiple Teams devices. You will need to evaluate different devices profiles and configure profile settings for the devices. At the end, you will need to evaluate the process of creating Microsoft Teams room, where multiple Teams rooms will be purchased in your organization.

## **Objectives**

After you complete this lab, you will be able to:

- Calculate the network bandwidth capacity for a Teams deployment

- Work with the Network Testing Companion on a client

- Create configuration profiles for devices

- Configure a new Microsoft Teams Room

## **Lab Setup**

- **Estimated Time:** 60 minutes.

## **Instructions**

Microsoft Teams provides users with chat, audio, video and content sharing experience in different network conditions. It includes variable codecs, where media can be negotiated in limited bandwidth environments. However, as a Teams admin, you will need to carefully plan your network bandwidth, because there are other Office 365 services and third-party apps that also need reliable network connection. Therefore, it is very important that Teams admins have tools that could help to estimate the bandwidth consumption according to specific business requirements and existing network infrastructure and provide best experience to business users.


```
Note : 
Please note that odl_userXXXXX@<YourTenant>.onmicrosoft.com is your administrator user and you should use odl_userXXXXX@<YourTenant>.onmicrosoft.com in place of MOD Administrator (admin@<YourTenant>.onmicrosoft.com) throughout this lab
```

#### Assign Teams Admin Roles to users

In this task, you will use the default global admin to login to the Microsoft 365 admin center and assign several teams admin roles to different users. This task is crucial for the following tasks and exercises because you will perform most of the tasks in context of Joni Sherman’s account.

1. Connect to the **Client 1 VM**, Sign in to the **Microsoft 365 admin center** ([**https://admin.microsoft.com**](https://admin.microsoft.com/)) using **MOD Administrator** (admin@&lt;YourTenant&gt;.onmicrosoft.com).

2. Assign the role of the **Teams Administrator** to **Joni Sherman**.

3. Assign the role of the **Teams Device Administrator** to **Alex Wilber**.

4. Assign the role of the **Teams Communication admin** to **Allan Deyoung**.

5. Leave the client open at the **Microsoft 365 admin center**.

You have now successfully assigned the Teams admin role to Joni Sherman and the Teams communications support engineer to Allan Deyoung. Proceed to the next task.

#### Check license assignment of your users**

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


### Create groups and teams

In this exercise, you will create some resources required in later tasks. These include creating a Microsoft 365 Group from the Microsoft 365 admin center and creating a team in the Desktop client and then the web client.

#### Create a Microsoft 365 Group

In real world scenarios, the Microsoft 365 Groups would already exist and your task as Teams Administrator would only be to enable their Teams functionality, but for this lab you need to create them manually.

You will create the new Microsoft 365 Group named "IT-Department" and then add the pilot members serving as a basis for your future teams and licensing.

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

#### Create a new team by using the desktop client

To test the self-service capabilities of Teams, in this task, Megan Bowen will sign in to the Teams Desktop client, create a new team with the name "Teams Rollout" and add all members participating in the Teams evaluation project.

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

#### Create a new team by using the web client

In this task, Lynne Robbins will continue testing the self-service capabilities of Teams by using the Teams web client to create another team with the name "Sales". She will also add Megan Bowen as a member.

1. Connect to the **Client 2 VM** with the credentials that have been provided to you.

2. Browse to the **Microsoft Teams web client** at [**https://teams.microsoft.com**](https://teams.microsoft.com/) and sign in as **Lynne Robbins** (LynneR@&lt;YourTenant&gt;.onmicrosoft.com).

4. Select **Join or create a team** from the lower left corner. 

5. Select **Create team** >**From scratch** > **Private**. Enter the team name **Sales** and select **Create**.

6. On the **Add members to Sales** window, enter the following names and select **Add** > **Close**.

    * Megan Bowen

The newly created team is displayed in the list of your teams. You have successfully created a new team with the Teams web client. 

### **Exercise 1: Calculate networking capabilities**

#### Task 1 - Calculate network bandwidth capacity

In this exercise, you will calculate the network requirements for Microsoft teams, depending on your expected Teams usage business requirements. You must ensure enough bandwidth based on your organization network connectivity that is described in the following table:

| **Location**| **Total number of employees**| **WAN link capacity / audio/video queue size (Mbps)**| **Office 365 connection**| **Internet connection** |
| - | - | - | - | - |
| New York HQ| 1000| 1000/300/500| ExpressRoute| Local Internet 1000 Mbps |
| Los Angeles Office| 250| 500/100/200| Remote connection through HQ| Remote Internet through HQ |
| Houston Office| 150| 400/50/100| Remote connection through HQ| Remote Internet through HQ |


Next, you will analyze your current bandwidth usage and test your network quality and connection to Microsoft Teams. You will also need to troubleshoot potential voice quality issues.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. Sign in to the **Teams admin center** ([**https://admin.teams.microsoft.com/**](https://admin.teams.microsoft.com/)) using **Joni Sherman** (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).

3. In the **Teams admin center,** on the left-hand navigation pane, expand **Planning**, and select **Network Planner**.

4. On the **Network planner** page, under **Network plans** tab, select **Add**.

5. On the **Network plan name** page, in the **Network plan name** box, type **Contoso plan**, and in the **Description** box type **Contoso Teams Network plan**, and then select **Apply**.

6. On the **Network planner** page, select **Personas** tab, and then select **Add**.

7. On the **Add persona** page, in the **Persona name** box type **New York office**, in the **Description** box type **New York office Teams users**, under the **Permissions** section, turn **On** all buttons, and then select **Apply**.

8. Select **Add** again, and on the **Add persona** page, in the **Persona name** box type **Los Angeles office**, in the **Description** box type **Los Angeles office Teams users**, under the **Permissions** section, turn **Off PSTN** button, and turn **On** all other buttons, and then select **Apply**.

9. Select the **Networks plans** tab, then select **Contoso plan**, and under **Network sites** tab, select **Add a network site**.

10. On the **Network site** page, enter the following information:

	- In the **Network site name** field, type **New York HQ site**.

	- In the in the description field type **New York HQ site network infrastructure**.

	- In the **Network users** field type **1000**.

	- In the **Network settings** section, in the **Subnet** box type **172.16.0.0**, and in the **Network range** box type **16**.

	- In the **Network settings** section, turn **On** the **Express Route** button.

	- In the **Network settings** section, in the **Internet link capacity** box, type **1000**.

	- In the **Network settings** section, in the **PSTN egress** drop-down box, choose **Use VoIP only**, and then select **Save**.

11. On the **Contoso plan** page, under **Network sites** tab, select **Add a network site**.

12. On the **Network site** page, enter the following information:

	- In the **Network site name** field, type **Los Angeles site**.

	- In the in the description field type **Los Angeles site network infrastructure**.

	- In the **Network users** field type **250**.

	- In the **Network settings** section, in the **Subnet** box type **192.168.10.0**, and in the **Network range** box type **24**.

	- In the **Network settings** section, ensure **ExpressRoute** button is **Off**.

	- In the **Network settings** section, turn **On** the **Connected to WAN** button, then in **WAN link capacity** box type **500**, in the **WAN audio queue size** box type **100**, and in **Video queue size** box type **200**.

	- In the **Network settings** section, in the **PSTN egress** drop-down box, **choose VoIP only**, and then select **Save**.

13. On the **Contoso plan** page, under **Network sites** tab, select **Add a network site**.

14. On the **Network site** page, enter the following information:

	- In the **Network site name** field, type **Houston site**.

	- In the in the description field type **Houston site network infrastructure**.

	- In the **Network users** field type **150**.

	- In the **Network settings** section, in the **Subnet** box type **192.168.20.0**, and in the **Network range** box type **24**.

	- In the **Network settings** section, ensure ExpressRoute button is **Off**.

	- In the **Network settings** section, turn **On** the **Connected to WAN** button, then in **WAN link capacity** box type **400**, in the **WAN audio queue size** box type **50**, and in **Video queue size** box type **100**.

	- In the **Network settings** section, in the **PSTN egress** drop-down box, **choose VoIP only**, and then select **Save**.

15. On the **Contoso plan** page, select **Report** tab and then select **Start a report**.

16. On the Report page, in the **Report name** field, type **Contoso report,** and in the description field, type **Contoso network estimation report**.

17. Under the **Calculation** section, review the default distribution of different personas in each site, and then select **Generate report**.

18. Under the **Reports** section, review the impact of Microsoft Teams on the Contoso network infrastructure by analyzing the report results on bandwidth needed for audio, video, screen sharing, Office 365 traffic, and PSTN.

19. On the report page, select the **Switch to chart view** at upper-right hand corner to display report results in different views.

Once you generate the report, you’ll see the recommendation of your bandwidth requirements. The allowed bandwidth shows how much of your overall traffic is reserved for real-time communications. Thirty percent is the recommended threshold. By changing this value and selecting **Run report**, you can see the different impact on the bandwidth for your network. Any areas that need more bandwidth will be highlighted in red. Work with your instructor to modify the parameters in the Network Planner and verify different results based on the input data.

In this lab, you have used Network Planner to estimate the Microsoft Teams impact on the bandwidth in your network infrastructure.

#### Task 2 - Use network testing companion

You are in the planning phase of a Microsoft Teams deployment. Before deploying Microsoft Teams in your organization, you want to test your network quality and connection to Microsoft Teams. After completing the test, you will interpret the results and gain insights into potential network issues.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. On the taskbar at the bottom of the page, right click the **Start** button and then select **Windows PowerShell (Admin)**.

3. Confirm the **User Account Control** window with **Yes**.

4. In the PowerShell window, enter the following cmdlet to install the Network Testing Companion:

   ```powershell
   Install-Module -Name NetworkTestingCompanion
   ```
5. Type in **y** and hit **return** for the Question with the **Untrusted repository**.

6. Enter the following cmdlet to create desktop shortcuts:

   ```powershell
   Invoke-ToolCreateShortcuts
   ```
7. Close the PowerShell window.

8. Open **Network Testing Companion** from the desktop shortcut and select the **Install** button, to install the Network Assessment Tool.

9. On the **User Account Control** window, select **Yes**.

10. Wait until window **Skype for Business and Microsoft Teams Network Testing Companion** initializes with green **Start** button appears in the **Network Connectivity and Quality Test** section on the right side of the window.

11. Review the information under **Windows operating system** and **Internet connection** sections and verify that no errors appear.

12. Select the green **Install** circle below **Network connectivity and quality test**.

13. A **User Account Control** window will appear in the taskbar. Maximize it and select **Yes.**

14. When the installation was successful, the symbol below **Network assessment tool** will change to a green checkmark in a circle too.

15. Select the green **Start** button in the **Network Connectivity and Quality Test** section to start the tests.
 
16. On the **Windows Security Alert** window, select **Allow access**. 

    >**Note:** If you receive a timeout message during the connectivity test, you can select the **Settings** tab in the tool. Adjust the **Connectivity test timeout (seconds)** option to a larger value and then start the test again.

17. When the tests have finished, the symbols below **Connectivity** and **Quality** will turn to green checkmarks in green circles.

18. After the test is **finished**, select the **View Results** tab and review the detailed results of the tests.

19. In the **View Results** tab, select **Report** file icon under **Network Connectivity** and **Network Quality** and review the testing steps and reports.

20. Discuss the results with the instructor.

21. Close all notepad windows and the **Skype for Business and Microsoft Teams Network Testing Companion.**

In this task, you have used Skype for Business and Microsoft Teams Network Testing Companion to test the connectivity and connection quality of your network infrastructure for Microsoft Teams.

### **Exercise 2: Deploy Teams device profiles**

As a Teams administrator, you will create configuration profiles to manage settings and features for Teams devices in your organization. You can create or upload configuration profiles to include settings and features you want to enable or disable and then assign a profile to a device or groups of devices.

Your organization could purchase Microsoft Teams Rooms that provide complete meeting experience with HD video, audio, and content sharing in conference rooms. You will need to prepare the deployment prerequisites by define Microsoft Teams Rooms service account in Office 365.

#### Task 1 - Create configuration profiles

During the planning phase of Teams Phones devices in your organization, you want to evaluate settings that can be applied to Teams devices by using configuration profiles in Teams admin center. You will create configuration profile for Teams device and analyze settings that will include in the configuration profile. Once devices are deployed into your organization, you will be ready to apply configuration profiles to those devices.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. Open **Microsoft Edge**, maximize the window and navigate to the **Teams admin center** at [**https://admin.teams.microsoft.com/**](https://admin.teams.microsoft.com/).

3. On the **Pick an account** page, select the **Joni Sherman** (JoniS@&lt;YourTenant&gt;.onmicrosoft.com) and sign in with the provided credentials.

4. In **Teams admin center**, on the left navigation pane, select **Devices**, and then choose **IP Phones**.

5. On the **IP Phones** page, select **Configuration profiles** tab, and then select **Add**.

6. Enter the following information for the new configuration profile:

	- Configuration profile Name: **New York Teams Desk Phones**

	- Description: **Configuration profile for Teams Desk Phones in New York HQ**

7. Under **General** section, configure following settings:

	- Device lock: **On**

	- Timeout: **30 seconds**

	- PIN: **123456**

	- Language: English **(United States)**

	- Timezone: **(UTC-5:00) Eastern Time (US and Canada)**

	- Date format: **MM/DD/YYYY**

	- Time format: **12 Hours (AM/PM)**

8. Under **Device settings** configure following settings:

	- Display screen saver: **On, Timeout 1 minute**

	- Display high contrast: **On**

	- Office hours: **08:00-17:00**

	- Power Saving: **On**

9. Under **Network settings**, configure following settings:

	- DHCP enabled: **On**

	- Logging enabled: **Off**

	- Device’s default admin password: **Pass@word1**

10. Once you complete with the configuration profile settings, select **Save**.

In this task, you have successfully created a configuration profiles that can be applied to Microsoft Teams devices.

#### Task 2 - Create a Microsoft Teams Room

Your organization has ordered devices for Microsoft Teams room. In the meantime, you need to ensure that all prerequisites for the equipment installation are being completed. One of the prerequisites for Microsoft Teams Room deployment is adding a device account and assigning Office 365 license for that account. Because you need to use the Exchange Online PowerShell to complete this task, you will first install the new Exchange PowerShell module.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. On the taskbar at the bottom of the page, right click the **Start** button and then select **Windows PowerShell (Admin)**.

3. Confirm the **User Account Control** window with **Yes**.

4. Enter the following cmdlet to install the Exchange PowerShell v2:

   ```powershell
   Install-Module ExchangeOnlineManagement
   ```
5. Confirm the Untrusted repository message with **y** for yes.

6. Close the elevated PowerShell window.

7. Right-click the Start button and select **Windows PowerShell.**

8. Enter the following cmdlet to connect to Exchnage Online PowerShell:

   ```powershell
   Connect-ExchangeOnline
   ```
9. When you see the **Sign in** window, enter admin@&lt;YourTenant&gt;.onmicrosoft.com and sign in with the credentials provided to you.

10. Create a new room mailbox named **NY-TeamsRoom1** by running the following cmdlet (remember to replace your tenant name):

    ```powershell
    New-Mailbox -Name "NY-TeamsRoom1" -Alias NY-TeamsRoom1 -Room -EnableRoomMailboxAccount $true -MicrosoftOnlineServicesID NY-TeamsRoom1@<YourTenant>.onmicrosoft.com -RoomMailboxPassword (ConvertTo-SecureString -String 'pass@word1' -AsPlainText -Force)
    ```
11. Configure the Calendar Processing features for the Teams Room. Read the following description and run the cmdlet at the end:

	- AutomateProcessing: **AutoAccept** (Meeting organizers receive the room reservation decision directly without human intervention: free = accept; busy = decline.)

	- AddOrganizerToSubject: **$false** (The meeting organizer is not added to the subject of the meeting request.)

	- DeleteComments: **$false** (Keep any text in the message body of incoming meeting requests.)

	- DeleteSubject: **$false** (Keep the subject of incoming meeting requests.)

	- RemovePrivateProperty: **$false** (Ensures the private flag that was sent by the meeting organizer in the original meeting request remains as specified.)

	- AddAdditionalResponse: **$true** (The text specified by the AdditionalResponse parameter is added to meeting requests.)

	- AdditionalResponse: **"This is a Teams Meeting room"** (The additional text to add to the meeting request.)
	
    ```powershell
    Set-CalendarProcessing -Identity "NY-TeamsRoom1" -AutomateProcessing AutoAccept -AddOrganizerToSubject $false -DeleteComments $false -DeleteSubject $false -RemovePrivateProperty $false -AddAdditionalResponse $true -AdditionalResponse "This is a Teams Meeting room"
    ```
12. Disconnect from Exchage Online and end the established session with the following cmdlet:

    ```powershell
    Disconnect-ExchangeOnline
    ```
13. Confirm the command with **y** for yes.

14. Connect to **Azure AD PowerShell** to configure Teams Room account settings by running the following cmdlets:

    ```powershell
    Connect-AzureAD
    ```
    When you see the Sign in window, type admin@&lt;YourTenant&gt;.onmicrosoft.com and sign in with the credentials provided to you.

15. Disable the password expiration for the Teams Room account **NY-TeamsRoom1** by running the following cmdlet:

    ```powershell
    Get-AzureADUser | Where {$_.DisplayName -eq "NY-TeamsRoom1"} | Set-AzureADUser -PasswordPolicies DisablePasswordExpiration
    ```
16. Close the PowerShell window.

17. Open **Microsoft Edge**, maximize the window and navigate to the **Microsoft 365 admin center** at [**https://admin.microsoft.com/**](https://admin.microsoft.com/).

18. On the **Pick an account** page, select the **MOD Administrator** (admin@&lt;YourTenant&gt;.onmicrosoft.com) and sign in with the provided credentials.

19. In the **Microsoft 365 admin center** from the left navigation pane, under **Billing** select **Purchase services**.

20. In the **Search** box on the right, type **Meeting Room** and then hit Enter.

21. In the results page, locate the **Collaboration and communication** section, and under **Microsoft Teams Rooms Standard** tile, select **Details** and then select **Get free trial**.

22. In the **Check out** page, select **Try now**, and in the **order receipt** page, select **Continue**.

23. In the **Microsoft 365 admin center** from the left navigation pane, select **Users**, and then choose **Active Users**.

24. Select the NY-TeamsRoom1@&lt;YourTenant&gt;.onmicrosoft.com account, and then select the **Licenses and Apps** tab.

25. In the NY-TeamsRoom1@&lt;YourTenant&gt;.onmicrosoft.com page, under the **Licenses and Apps** tab, select **Microsoft Teams Rooms Standard** and then select **Save changes**.

26. Close all open windows.

You have successfully created, configured, and licensed a Microsoft Teams Room service account, which is a prerequisite for deploying a Microsoft Teams Room system.

END OF LAB
