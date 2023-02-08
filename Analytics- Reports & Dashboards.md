# Gainsight Analytics- Reports & Dashboards

[Gainsight Study Table Of Contents](https://github.com/Zennewman/Gainsight-Resources/blob/a0f7078e046e4e025608988aa1ae274447bf401f/README.md)</br>
[Admin Guide for Horizon Analytics](https://support.gainsight.com/SFDC_Edition/Reports_and_Dashboards/Horizon_Analytics)</br>
[Gainsight Analytics Course](https://education.gainsight.com/page/analytics)</br>

-----

## Reporting Basics

### Use Cases 
* Prioritize books of business to surface accounts that are high risk, high value or in implementation for additional support and attention. 
* 1:1 meetings between managers and CSMs to review their book of business and the health and opportunities in their accounts. 
* Monitor risk by highlighting at-risk accounts and trends that point towards increases or decreases in risk. 
* Additional Use cases
	* Upcoming renewals
	* Product requests 
	* Open support tickets 

### Common Objects to Report On 
* **Company**: General customer information, including onboarding stage, number of employees, ARR, Current Score, Industry, Company Type, Renewal Date, Original Contract Date, etc.
* **Company Person**: General attributes of the person in relation to a company, including the status of a person, GSID, Role, etc.
* **Customers**: For general customer information such as Lifecycle Stage, # of Employees, etc.
* **NPS Survey Response**: Responded Date, Score Type, NPS Score, etc
* **Calls to Action**: For customized CTA reason/status/type reporting (Call to Action ID is a unique identifier for each CTA)
* **Opportunities**: For information such as Upsell, down-sell, and churn
* **User Adoption**: For Reporting against your usage data.

>[!Attention]
>Gainsight report builder only looks at one object at a time, but can be extended by [[Analytics-Data Designer]]


### How to Access Report Builder 
![How to access report builder](https://github.com/Zennewman/Gainsight-Resources/blob/97a3a3443ce183f3519cdfebf32df5827c4e50a1/Resources/3tCy79i3Nt7eK8Dk_AR56nsgukXPqBpGX%202.png)

![How to access report builder](https://github.com/Zennewman/Gainsight-Resources/blob/97a3a3443ce183f3519cdfebf32df5827c4e50a1/Resources/izjjbpIo7aO0wR7V_aD9KVv8F1K1YzzcT.png)


The reports page has two sections, a Reports List page where existing reports can be accessed and a settings page where data downloads etc. can be toggled on and off. 

#### Report List View 
Reports can be organized into folders. (best practice)

The list view can also be filtered to more quickly find reports

#### Report Settings Pages
- General Settings
* Chart Editor Settings
* Color Palette Settings
* Custom Colors
* Self Service Analytics (whether or not CSMs and other users can self-serve on reporting)

### Creating a Report
>[!Attention]
>Build a report in dev account and add screen shots

____________________________
## Advanced Reporting

### Aggregation Options For Fields
- **String/Text**: Count, Count Distinct
- **Numeric**: Count, Count Distinct, Min, Max, Avg, Sum
- **Boolean**: Count
- **Date**: Count, Count Distinct, Min, Max
- **DateTime**: Count, Count Distinct, Min, Max

Reports can be grouped at the row level. Pivot tables can also be created by grouping columns in addition to rows. 

The Pivot can be applied only on one field at a time. You can pivot reports on the entire dataset from the server-side. While there is no **row** limit for pivoted reports, the maximum number of **pivoted columns** visible in a report is 53. Pivot tables must have at least two fields in the group-by section. 

Decimals can be set to up to 3 places. 


### User Permissions & Self-Serve Analytics

Reporting can only be performed on the objects the user has access to. 

Four types of permission sets that can be granted: 
* **Report Builder User** allows users to create, edit and share reports in Gainsight
* **Dashboard Builder User** allows users to create private dashboards from reports. Dashboards can be shared individually, but can't be made public
* **Report Builder Admin** This permission gives full control to the end-users. They can access all the reports, settings, and view the reports as other users
* **Dashboard Builder Admin** This permission lets end-users create, assign and make the dashboards public.

Three types of navigation permissions that need to be granted in tandem with reporting permission types:  
* **Analytics** This permission gives users the ability to quickly build reports and add them to dashboards.
* **Reports** This permission allows users to build reports and visualize data, add them to 360, dashboards, and embed them in emails.
* **Dashboard Builder** This permission lets users build dashboards and assign dashboards to a user or user group.

These two permission set groupings can be paired with Object level access for granular access control. 

Managing Object Access to Users: 
1. Click Settings from the report tab
2. Click Self-Service Analytics
3. Select Specify Objects
4. Select the users to grant access to
5. Select either **All Objects** or specify which objects users should have access to
6. Save

Be default, users the admin has granted view access to and users the admin has granted view/edit access to have view all permissions on dashboards.  

>[!Attention]
>#### Points to Remember
>- If an object has a lookup relation with another object, you will have to grant access to both the objects for a CSM to create or edit reports on lookup fields. For example, if a CSM wants to create a report on lookup fields of Company from Company Person, you would have to assign both the objects to the user.
>
>- Assigning an object will not override any data permissions that have been set up already. For example, if a CSM doesn't have READ/WRITE data permissions for a specific object, they wouldn't be able to create a report on that object even if you have assigned the object.
>
>- It's not possible to restrict permissions at the field level.


### Using Formulas in Reports 

[Gainsight Documentation](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/User_Guides/05_Formula_Fields_in_Reporting)
>1.  Navigate to **Administration > Report Builder**.
>2.  Click on the existing report or click **Create Report** to create a new report.
>3.  Select the required **Object** on which you want to create a report.
>4.  Click **Add Formula Field**. The **Add Formula Field** page appears.  
    **Note**: Formula fields cannot be used in reports created on SFDC objects.
>5.  Populate the following details:
    1.  **Label**: Enter the name of the Formula Field.
    2.  **Data Type**: From the **Data Type** dropdown list, select the required data type (_String, Date_, _Number_).  
        **Notes**:
			-Select the data type, based on the output field you want. For example, if you want to see the output as number of days/weeks/months, then select the output data type as a number.
			-Functions_ and _Fields_ may differ based on the selection of the data type.
> 3.  Select the required **Function** of your choice, and then enter the _Values_ and/or _Fields_ as per your requirement.
>1.  Click **Save**.


## Dashboards

[Gainsight Documentation](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/User_Guides/08_Configure_Dashboards)

The layout page has two sections:
1. Adoption Explorer, Renewal Center, Reports, Scorecard Widgets and Standard Widgets pane
2. Dashboard layout pane

![Dashboard design pane](https://github.com/Zennewman/Gainsight-Resources/blob/97a3a3443ce183f3519cdfebf32df5827c4e50a1/Resources/Dashboard%20Builder%202022-02-03%20at%2011.05.55%20AM%20(1).png)


Admins can add **Reports**, **Adoption Explorer**, **Standard**, and **Scorecard Widgets** into the Dashboard layout pane, edit, resize, reposition, and delete in the layout pane as required. In addition, images, website iframes and rich text widgets can be added to the dashboard layout. [Information on how to configure each is detailed here](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/User_Guides/08_Configure_Dashboards). 

Widgets can be added from the widget dropdown on the left side of the palette. Once added, they can be dragged around the palette and resized as needed. To view the widgets with actual data, toggle the live data switch at the top of the palette. 

### Dashboard Sharing Documentation
[Dashboard Sharing](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/User_Guides/Share_Dashboards_(Horizon_Analytics))
[Dashboard Permissions](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/Admin_Guides/02_Dashboard_Permissions)
[Configure Dashboard Sharing](https://support.gainsight.com/Gainsight_NXT/Reports_and_Dashboards/User_Guides/10_Configure_Dashboard_for_Sharing)


