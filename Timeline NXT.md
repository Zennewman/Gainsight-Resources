# Timeline NXT
[[Gainsight Study Table Of Contents]]

## Resources 
[Configure Associated Records to Timeline](https://support.gainsight.com/SFDC_Edition/Timeline/Admin_Guides/Configure_Associated_Records_to_Timeline)
[Configure Timeline View for C360](https://support.gainsight.com/SFDC_Edition/Timeline/Admin_Guides/Configure_Timeline_View_for_C360_and_R360)
[Configure Associate Records to Timeline](https://support.gainsight.com/SFDC_Edition/Timeline/Admin_Guides/Configure_Associated_Records_to_Timeline)
[Timeline Overview](https://support.gainsight.com/Gainsight_NXT/Timeline/02Admin_Guides/Configure_Timeline_Settings)
[Configure Milestone Types](https://support.gainsight.com/Gainsight_NXT/Timeline/02Admin_Guides/Configure_Manual_Milestone_Types)

## Course Material 
### Introduction 
----
### From the Documentation
**Timeline** is an official record of your customers. It allows users to log information on customer interactions in a way that enables you to quickly gather insights and drive action. For more information, refer to the _[Timeline Overview](https://support.gainsight.com/Gainsight_NXT/Timeline/01About/Timeline_Overview "Timeline Overview")_ article.

To configure the Timeline general settings, navigate to **_Administration > Timeline > GENERAL SETTINGS._** 

General Settings in the Timeline Admin page consists of various configurations like enabling Timeline, creating and editing activity types, reporting categories, and additional settings. You can configure activities either globally or at the Company or Relationship level.

**Suggested Usages for the Timeline**
-   Weekly updates on the Customer’s status and recent events for every customer.
-   Document all emails, calls, or meetings with the customer that should be recorded in the Customer’s history, along with the corresponding notes.
-   When ownership transitions occur, or new owners are introduced, Timeline can provide an easily digestible history with rich context to get the new owner up-to-speed.
-   When Executive Sponsors or Leaders meet with a customer, they can review the Timeline to understand the customer’s history and context.
-   Meeting preparation: Create a draft activity and add your meeting agenda. During the meeting, use the same list to guide the meeting and increase your note-taking efficiency. ("Log" the activity if you want your colleagues to be able to see it prior to the meeting.)
-   If your organization uses an external note-taking solution, such as Evernote, the Timeline feature is a good alternative since the information is visible to all Gainsight users in C360.

-------

**Additional use cases**
- Create customer health score measurements
- Use Days Since Last Timeline and Days Since Last Exec Touchpoint metrics in timeline reporting 
- Assign CTA to CSM/Executive after certain number of days since last touch 


**Default Activity Types
- Calls
- Updates
- Meetings
- Emails 
- Milestones

### Configuring the Timeline
**Navigation** 
Administration -> Timeline 
![[Pasted image 20221005113026.png]]

Additional activity types can be added. They can be created globally, for companies or relationships. 

Milestones can also be created. These indicate major events in the companies lifecycle such as renewals, QBRs and project kickoffs. 

![[Pasted image 20221005113849.png]]

Steps to create a new milestone: 
1.  In the Name field, enter a name for the Milestone Type.
2.  Select a color from the color palette.
3.  Select the **Active** checkbox to set the Milestone type to active status.
4.  Click **SAVE**.

[Configure Milestone Types](https://support.gainsight.com/Gainsight_NXT/Timeline/02Admin_Guides/Configure_Manual_Milestone_Types)

### Configuring Associated Records

Timeline activities can be associated with more than one record, for example with contacts as well as the company. 

Associated records can be made available to CSMs in the following ways: 
-  Adding Associated Records to all Activity Types. This is the quickest way to enable associated records within your org. Associated records will be enabled, and an Associated Record field will be added to all Activity Types. 
- Adding Associated Records to a specific Activity Type

To add associated records to specific activity types:
1. Navigate to Administration -> Timeline
2. In the Introducing Associated Records section, for the question **Do you want to add the Associated Record field to all Activity Type forms?** select **No, I'll add manually**.
3. Click the **ENABLE ASSOCIATED RECORDS** button.
4. Click edit in the activity type list on the activity type desired
5. Configure the layout to include the Associated Records 


![[wQjricyWWR-T5AfU_c6Yh8bh0s4ZsJ9ZL 1.png]]
![[dhWQ8D_DOSXTgcqp_xq2K_xYWdWmxHZM9.png]]

**Configure Search Fields and Filters** 

Here, additional objects can be enabled as associated records. Both objects and the fields they're searchable by can be activated and deactivated. 

By default, the following records are activated:
-   Call to Action
-   Case (Enabled only if the Cases Object has been enabled in the Customer's tenant. The  Case object also gets enabled when there is Zendesk connection in Customer's instance.)
-   Company
-   Relationship

![[Pasted image 20221005115013.png]]

### Gong Integration with Timeline 

>With Gainsight's integration with Gong.io, Gong call recordings are logged directly to Timeline. This allows CSMs to capture and analyze conversation sentiment and keywords which can then be leveraged to drive the right actions.
>
>Critical meeting data such as the title of the meeting, important keywords (trackers), meeting recording, and internal and external attendee details are captured within the Activity. A new Activity is created in Timeline for each meeting that is synced from Gong.

**Gong can be configured from the Connectors 2.0 section under administration**

**Navigation:** Administration -> Connectors 2.0 -> Create Connection

[Configure Gong Integration Settings](https://support.gainsight.com/Gainsight_NXT/Timeline/02Admin_Guides/Configure_Gong_Integration_Settings)

![[Pasted image 20221005115912.png]]

### Creating Templates for Activity Timeline Notes 

Notes can be templated to provide a consistent format and ensure that the needed information is being captured. Admins can create and distribute notes across the entire organization. 

**Navigation** Administration-> Timeline-> Note Template

[Configure Note Templates](https://support.gainsight.com/Gainsight_NXT/Timeline/02Admin_Guides/Configure_Note_Templates)

### Quiz 
1. **Q** Timeline is a tool that allows customer interactions to be tracked to provide visibility across the organization.
	1. **A** TRUE
2. **Q** Timeline:
	1. **A** Is a centralized location for Calls, Updates, Meetings, Emails, Milestones
	2. **A** Provides visibility, minimizing requests for updates
	3. **A** Simplifies account transition
	4. **A** ==All of the above
3. **Q** What are the standard Activity Types? Select all that apply
	1. **A** Calls
	2. **A** Updates
	3. **A** Meetings
	4. **A** Emails
	5. **A** Milestones
	6. **A** ~~Escalations~~
4. **Q** Activity types can be configured at what levels? Select all that apply.
	1. **A** Global
	2. **A** Company
	3. **A** Relationship
	4. **A** ~~Company Person~~
5. **Q** You can create custom Activity types to meet the needs of your organization.
	1. **A** TRUE 
