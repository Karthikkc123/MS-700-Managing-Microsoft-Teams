

# **Lab 05: Modify collaboration settings for Teams**

## **Lab Scenario**

In managing collaboration in Microsoft Teams, you will manage chat and collaboration experiences such as team settings or private channel creation policies. Finally, you will manage settings for Teams apps such as app setup policies, Apps, bots & connectors in Microsoft Teams or publish a custom app in Microsoft Teams.

## **Objectives**

After you complete this lab, you will be able to:

- Create a messaging policy

- Manage private channels

- Disable third party storage providers

- Create a Power Apps app

- Manage Policy packages

- Upload a tenant wide custom line of business app

- Edit and test default org-wide app policy

- Edit and test default app permission policy

## **Lab Setup**

- **Estimated Time:** 90 minutes.

## **Instructions**


```
Note : 
Please note that odl_userXXXXX@<YourTenant>.onmicrosoft.com is your administrator user and you should use odl_userXXXXX@<YourTenant>.onmicrosoft.com in place of MOD Administrator (admin@<YourTenant>.onmicrosoft.com) throughout this lab
```

### **Exercise 1: Configure channel and message policies**

In this exercise you will configure policies to manage the creation of new private channels and the available tools for users in chat.

#### Task 1 - Create messaging policy for giphy, memes and stickers

In the past, some users of Contoso have used a lot of stickers, gif animations and similar pictures in their conversations, even with externals using other chat solutions. The new corporate guideline shall prohibit the use of graphic elements in corporate communication via Teams, because users shall not use them in conversations with external customers and clients. As a Teams service administrator, you must create a new message policy that prohibits its use and apply it to several users of your pilot project.

**Note:** After creating a messaging policy, it can take up to 24 hours for the settings to be applied to the users.

1. Connect to the Client 1 VM with the credentials that have been provided to you.

2. Open **Microsoft Edge**, maximize the window and navigate to the **Teams admin center** at [**https://admin.teams.microsoft.com/**](https://admin.teams.microsoft.com/).

3. On the **Pick an account** page, select the **Joni Sherman** (JoniS@&lt;YourTenant&gt;.onmicrosoft.com) and sign in with the provided credentials.

4. In the left-hand navigation pane, select the **Messaging policies**, then click on the **+ Add** at the right side of the page, to create a new messaging policy.

5. In the **New messaging policy** dialog enter the following information to the fields and set the following configuration:

	- **Name**: Regular users without fun stuff

	- **Description**: Policy to disable giphys, stickers, and memes in conversations

	- **Use Giphys in conversations**: off

	- **Use Memes in conversations**: off

	- **Use Stickers in conversations**: off

6. Leave the rest of the settings as default. Select **Save**.

7. In the Messaging policies overview, select the checkmark left to **Regular users without fun stuff**. Then select **Manage users** in the top navigation pane. If you cannot see **Manage users**, you may need to select the three dots first.

8. Type in **Lynne Robbins** and select **Add**, and then select **Apply**.

9. Stay in the Teams admin center and continue with the next task.

In this task, you have successfully configured a new messaging policy and assigned it to Lynne Robbins. It will now take some time for the policy to take effect. Continue with the next task.

#### Task 2 - Manage private channels in a team

As Teams administrator of Contoso, you will create a private channel "confidential" in the sales team that only allows some people to be able to access the information.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. You are still signed in as **Joni Sherman** in the **Microsoft Teams Admin center**.

3. In the left-hand navigation pane, select **Teams** to open the menu and **Manage teams** below.

4. Select the **Sales** team in the **Manage teams** overview window.

5. Select the **Channels** tab in the middle of the page. Select **+ Add** in the navigation pane below to get into the **Add channel** window.

6. In the **Add channel** window enter the following information:

	- **Name:** Confidential sales

	- **Description:** Confidential private sales channel

	- **Type:** Private

7. Enter to the field **Channel owner** the user **Lynne Robbins** and select her as owner.

8. Select **Apply** in the **Add channel** window.

9. Connect to the **Client 2 VM** with the credentials that have been provided to you.

10. Open the Edge browser with the icon from the taskbar.

11. In your browser, select the address bar and go to the **Teams Web Client** page by entering the following URL: [**https://teams.microsoft.com**](https://teams.microsoft.com/)

12. On the **Pick an account** page, select the **Lynne Robbins** (LynneR@&lt;YourTenant&gt;.onmicrosoft.com) and sign in with the provided credentials.

13. On the Microsoft Teams landing page click **Use the web app instead**.

14. On the team overview in the Teams web client, you should see the new private channel **Confidential sales** with a small padlock icon.

In this task you learned how to create a private channel in the Microsoft Teams Admin center and how to configure and check the access.

### **Exercise 2: Manage app settings**

#### Task 1 - Disable third party storage providers

In the past, users stored data at various locations, including third-party storage providers. Recently, the company deployed OneDrive for all users and would like to guide the users to use SharePoint and OneDrive as the primary data storage locations with Box as an alternative for all file collaborations. As the Teams admin, you are asked to deactivate all third-party storage providers except Box in Microsoft Teams to align with the direction.

**Note:** After disabling the third-party storage provider, it can take up to 24 hours for the settings to be applied to the teams.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. You are still signed in as **Joni Sherman** in the **Microsoft Teams Admin center**.

3. On the left-side navigation pane, select the **Org-wide settings** to open the menu, then select **Teams settings** below.

4. In the Teams settings overview go to the **Files** section. Configure the following file sharing and cloud file storage options.

	- **Citrix files:** Off

	- **DropBox:** Off

	- **Box:** On

	- **Google Drive:** Off

	- **Egnyte:** Off

5. After this scroll down and select **Save**.

In this task you have learned how to enable or disable third-party storage providers for your whole tenant.

#### Task 2 - Edit default org-wide app policy

In the pilot project, the company decided that Microsoft Planner is the default app for all (existing) teams. To do this, edit the default org-wide app policy. This task may take some time to propagate throughout the tenant.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. You are still signed in as **Joni Sherman** in the **Microsoft Teams Admin center**.

3. In the left-hand navigation pane, select the **Teams apps** to open the menu, then select **Setup policies**.

4. In the **App setup policies** window select **Global (Org-wide default)** name to open the org-wide app policy.

5. In the **Pinned apps** section select **+ Add apps** to open the **Add pinned apps** menu at the right side.

6. Select **Global** and type in the name **Planner**, mouseover the presented name and select **Add**. After this, select **Add** to return previous window.

7. Make sure that **Planner** is now listed in the **Pinned apps** section and select **Save**.

8. In the **App setup policies** window select **Global (Org-wide default)** and make sure there is a selected checkmark in the front of the name.

9. Then select **Manage users** in the top navigation pane to open the **Mange users** dialog. Enter the name of **Lynne Robbins** and mouseover the presented name and select **Add**. Then select **Apply**.

10. Connect to the **Client 2 VM** with the credentials that have been provided to you.

11. Open the Edge browser, select the address bar and go to the **Teams Web Client** page by entering the following URL: [**https://teams.microsoft.com**](https://teams.microsoft.com/)

12. On the **Pick an account** window, select LynneR@&lt;YourTenant&gt;.onmicrosoft.com and sign in.

13. On the Microsoft Teams landing page click **Use the web app instead**.

14. In the left-hand navigation pane, the **Planner** app should be displayed by default below the Files **menu**.

#### Task 3 - Edit default app permission policy

In this task you will edit the default app permission policy and block the Google Analytics app for all tenants

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. You are still signed in as **Joni Sherman** in the **Microsoft Teams Admin center**.

3. In the left-hand navigation pane, select the **Teams apps** to open the menu, then select **Permission policies**.

4. In the **App permission policies** window select **+ Add** to create a new policy.

5. After this the policy creation dialog appears, type in the policy name **Block Google Analytics** and expand the menu in the **Third-party app** section, and select **Block specific apps and allow all others**.

6. Select **Block apps** below the Notification **Add apps that you want to block** to open the right-side menu.

7. In the Add third party apps dialog, type in **Google Analytics**, mouseover the presented name and select **Add**. Repeat the same step for **Google Analytics Insights**. After this select **Block** to return to the **App permission policies** window. Select **Save**.

8. In the App permission policies overview, select the checkmark left to **Block Google Analytics**. Then select **Manage users** in the top navigation pane.

9. Type in **Lynne Robbins** and select **Add** by mouseover the presented name, then click **Apply**.

In this task you have learned how to block the Google Analytics app for your tenant.

#### Task 4 – Manage policy packages

To avoid administrative overhead with managing large numbers of policies individually for groups of different users, you need to evaluate using policy packages to group policies into logical units. In this task you need to review the default policy packages and change a default policy package for first line workers.

1. Connect to the **Client 1 VM** with the credentials that have been provided to you.

2. You are still signed in as **Joni Sherman** in the **Microsoft Teams Admin center**.

3. In the left-hand navigation pane, select **Policy packages** to display existing policy packages.

4. Review the existing policy packages. Afterwards select **Frontline worker** to edit the policy package.

5. From the list of assigned policies, select **Frontline_Worker** right from **Messaging policy**.

6. Select **Edit** from the upper right corner to change the policy settings.

7. Select the switch right from **Send urgent messages using priority notifications** to **On** and select **Save**.

8. Back on the list of assigned policies, select **Frontline_Worker** right from **Calling policy**.

9. Select the switch right from **Prevent toll bypass and send calls through the PSTN** and **Busy on busy is available when in a call** to **On** and select **Save**.

10. Back on the list of assigned policies again, select **Back** to go to the Policy packages overview.

11. The checkmark left from the **Frontline worker** policy package is still active. Select **Manage users** from the top pane to open the **Manage users** right-side pane.

12.  Type "Allan" into the search bar, select **Add** right from **Allan Deyoung** and **Apply**.

13. Select **Users** from the left-side pane.

14. In the line of Allan Deyoung, select **View policies**.

15. Below Assigned policies you can now see the different **Frontline_Worker** policies and below **Policy package** the **Frontline worker** package.

You have successfully modified included policies from an existing policy package and assigned the package to a single user. This will help you assign the same set of policies to a group of users working in the same role or requiring the same access.

#### Task 5 - Built a flow using Power Automate in Teams

In this task, you will create an issue report system by using Power Automate in Teams. When users fill out the form from the **Contoso** org-wide team, the flow will send a message to notify members in the **IT-Department** team. 

1. Connect to the **Client 1 VM**.

2. Create a form

	1. Browse to the Forms web client (https://www.office.com/launch/forms) as **Joni Sherman**  (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).
	
	2. In the Froms web client, select **+ New Form**.

	3. Select on **Untitled form** and enter the following information:
	
		* Input your title here: **Submit a ticket**.
		* Enter a description: **Please provide the information. Our member from IT-Department will contact you as soon as possible.**

	4. Select **+ Add new** > **Text**.
	5. In the question textbox, enter **What is the issue?**

3. Install **Power Automate** in Teams. 

	1. Browse to the Teams web client (https://teams.microsoft.com/) as **Joni Sherman**  (JoniS@&lt;YourTenant&gt;.onmicrosoft.com).

	2. In left navigation of the Teams client, select **Apps** and search for **Power Automate**.

	3. Select **Power Automate** app, and select **Add**

4. Create a flow

	1. In left navigation of the Teams client, select **Power Automate**.

	2. Select **Create** tab from the top menu. 

	3. Select the template **Notify a team when a new Forms response is submitted** and select **Continue**

	4. Enter the flow name : **Report issue**. Select **Continue**.

	5. On the **Set up your flow** page, 
	
		* From the **The ID of the form you want to monitor** dropdown menu, select **Submit a ticket**. 

		* From the **Team to notify** dropdown menu, select **IT-Department**.

		* From the **Channel to notify** dropdown menu, select **General**.

	6. Select **Create flow** > **Done**

5. Add the form to the **General** channel of **Contoso** team.

	1. Go to the **General** channel of **Contoso** team.
	2. Add a tab by selecting **+** next to Wiki tab. 
	3. Select **Forms** from the **Add a tab** window. 
	4. Select **Add an existing form**, and select **Submit a ticket**.	
	5. Select **Save**.

6. Test the flow

	1. In the **General** channel of **Contoso** team, select **Fill|Submit a ticket** tab. 
	2. On the **Submit a ticket** page, enter the following to the textbox:
	
		*I need help to create a team for external partners.*  
	3. Select **Submit**.
	4. Go to the **General** channel of the **IT-Department** team. You will see a post via Power Automate. 

In this task, you have successfully created a flow from Power Automate in Teams, which notify the members in IT department when users submit a request ticket.

### **Exercise 3: Test configured policy settings**

In this exercise, you will test the configured policy settings on a client with the affected user Lynne Robbins and compare the settings to the available client settings of Joni Sherman.

#### Task 1 – Test the messaging policy and private channel access

In this task, you will test the **messaging policies** configured in exercise 1 and compare the difference between affected user (Lynne Robbins) vs regular user(Joni Sherman).

1. Connect to the **Client 2 VM** with the credentials that have been provided to you.

2. Select the **Edge Browser** icon from the taskbar. In your browser, go to the **Microsoft Teams web client** page by entering the following URL in the address bar: [**https://teams.microsoft.com/**](https://teams.microsoft.com/)

3. On the **Pick an account** page, select the **Lynne Robbins** (LynneR@&lt;YourTenant&gt;.onmicrosoft.com) and sign in with the provided credentials.

4. On the Microsoft Teams landing page click **Use the web app instead**.

5. Skip a potential welcome dialog by selecting on **x** in the right corner.

6. In the left-hand navigation pane, select **Chat**, then select the **Contacts** in the dropdown menu.

7. If there is no contact for **Joni Sherman**, then select **…** and select **Add a contact to this group**. Type in the name **Joni Sherman** and select her by mouseover the presented name. After this select **Add** to return to the **Contacts tab**.

8. In the **Contacts** tab, select **Joni Sherman**. Note that if the **giphy**, **memes** and **stickers** icons are missing below the conversation-bar, the **messaging policy** has taken effect.

9. In the left-hand navigation pane, select **Teams**.

10. Select the **Confidential sales** channel of the **Sales** team and add a comment to confirm that you have access to the private channel.

#### Task 2 – Test the app permission policy and storage providers

In this task, you will test the **app permission policies** configured in exercise 2 and compare the differences between affected user (Lynne Robbins) vs regular user (Joni Sherman).

1. Connect to the **Client 2 VM** with the credentials that have been provided to you.

2. You are still in the **Teams web client** and signed in as **Lynne Robbins**.

3. In the left-hand navigation select **Teams** and select the **IT-Department** channel **General**. Mouseover the presented name **General**, select **…** and then select **Connectors**.

4. In the **Connectors for "General"** window, enter **Google Analytics** into the search field.

5. If you can’t find **Google Analytics** as a search result and can’t add the app to the channel, the **app permission policy** has worked as desired.

6. In the left-hand navigation pane, select **Teams**, then select the **IT-Department** team. Select the **files** Tab on the middle of the Teams web client. Then select **+ Add cloud storage** in the navigation pane below.

7. If you only see SharePoint and Box as options, the cloud file storage settings in Teams settings worked as expected.

8. Sign out of Teams and close all open windows.

END OF LAB
