# Admin Cockpit & Playbooks
## Resources 
[How to Configure Cockpit and CTAs](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/How_to_Configure_Cockpit_and_CTAs_(path))



## Overview

The cockpit is the primary workspace for CSMs and Account Managers. The goal in customizing it is to create a streamlined display of the work that is due and what is upcoming. 

**Three Key Components of the Cockpit**
- Calls to Action
- Tasks
- Playbooks

| CTAs                |  Tasks                  | Playbooks                 |
|----------------|--------------------|------------------------|
|Lifecycle Driven Alerts that can be created automatically or manually CTAs contain subtasks as part of a Playbook. | Tasks are specific actions that need to be taken. | Playbooks are a predefined collection of tasks that are served during a CTA. |
|**Example** Upcoming renewal, client implementation | **Example** Call client, review NPS outcomes | **Example** Upsell opportunity:<br/> - loop in AE<br/> - set meeting with decision makers<br/> -create presentation |

### CTA Types 

**Activity** default activity type for CTAs created from the timeline.

**Risk** triggered based on negative trends/health scores that indicate an account might be at risk of churning. 

**Lifecycle** Typically time-based scheduled events that trigger at key points of the client lifecycle, for example onboarding, post implementation, etc.   

**Objective** Tied to success plans and can only be created from the C360 Success Plan section. 

**Custom CTAs** Examples include reference management and custom renewal CTAs that aren't otherwise fall under Lifecycle. 

### Creating CTAs 

CTAs can be created directly from the Cockpit or from the cockpit tab in the C360 layout. If CTAs are created from the C360, they'll have the company field automatically populated. If created from the Cockpit, the relationship will need to be manually selected in order to save the CTA. 

To save a CTA, the Company, Owner, Type, Priority, Reason and Status must all be populated. A playbook can be added if applicable. 
![[Pasted image 20221006110448.png]]

![[Pasted image 20221006110805.png]]

 **Example Business Use Case For Manually Created CTAs:** A user wants to track an important meeting, a customer event, or a risk that is identified. In such scenarios, they can create manual CTAs and Tasks, not only to track important initiatives but also to provide their team visibility into their workload.

### Tasks
>Tasks are the specific actions that must be completed in order to close a CTA. Typically working a CTA involves completing multiple tasks in a sequential order. Tasks can be manually added to a CTA, or can be added as a Playbook. We'll talk more about Playbooks in the next section.
>
   Admins are responsible for configuring the fields and layout of Tasks. If needed, Admins can create "Custom Fields" for Tasks, which allow for greater detail and visibility in reporting. We will cover Task Configuration in detail later in the course.


>[!Question]
>Do all tasks need to be under a CTA, or can they be standalone? 

### Playbooks 

Playbooks are task templates that can be attached to CTAs 

-----
**From the Documentation**
Benefits of using Playbooks include:

-   Drive consistency across the organization by creating standardized processes
-   Provide additional support to CSMs through embedded email templates and links to resources
-   Make it easier to onboard new CSMS by providing your organization's established best practices for working CTAs
-   Help your organization evolve and learn as Playbooks  are updated with the strategies used by your best CSMs

While the same Playbook can be used for multiple CTAs, a CTA can only have one active Playbook assigned to it.

Playbooks don't necessarily have to be created and edited by the Admin. As the Admin, you have the ability to set permissions to allow other users to create and edit Playbooks.

---- 

**Navigation**
Administration -> Cockpit -> Playbook

![[Pasted image 20221006112253.png]]

### Quiz
1. **Q** CTA stands for...
	1. **A** Call to Action
2. **Q** Match the definition to the correct term.
**A**  ![[Pasted image 20221006112517.png]]
3. **Q** What level can CTAs be configured at?
	1. **A** Company
	2. **A** Global
	3. **A** Relationship
4. **Q** True or False:  Admins have the ability to set permissions to allow other users to create and edit Playbooks
	1. **A** True

## Configuration 
**Documentation**
[How to Configure Cockpit and CTAs](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/How_to_Configure_Cockpit_and_CTAs_(path))
[Creating and Closing CTAs from the Rules Engine](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/Creating_and_Closing_CTAs_from_Rules_Engine)
[Configure CTA Detail View Layouts](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/Configure_CTA_Detail_View_Layouts)
[Configure CTA Linked Objects](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/Configure_CTA_Linked_Objects)

### How to Create New CTAs

**From the Documentation**
>For each CTA, you can customize options such as CTA Status, CTA Priority, and Snooze Reasons to fit your organization's use cases. You can also edit  the **Reporting Categories** for each option to ensure that  your reporting reflects an accurate picture of the data. 
>
For example, you may want to use the Reporting Category of "Open" for all open CTAs, regardless of the current status, so your reporting reflects how many open CTAs you have.

Five out of the box CTA Types: 
* Risk
* Objective
* Expansion
* Lifecycle 
* Renewals

>[!Attention]
>This contradicts the information above in [[Admin Cockpit & Playbooks#CTA Types]]

Up to 45 CTA types can be added, but the number should be limited as a best practice. 

**Adding New CTAs** 

**Navigation** Administration -> Cockpit -> Call to Action ->+Type 

![[Pasted image 20221006114248.png]]

New reporting categories can be added by clicking the Reporting Categories button next to +Type. Reporting categories determine how CTAs are grouped for reporting purposes. 

### Customizing the Fields that are Visible on the CTA

Scrolling down the Call To Action page will take you to a section called Detail View Layout Configuration. This is where the fields displayed on the CTA can be configured via drag and drop. 

![[Pasted image 20221006115202.png]]

Scrolling further down the page, there is a section for adding custom fields. This is where new fields can be created prior to adding them to the CTA layout. 

![[Pasted image 20221006115222.png]]
![[Pasted image 20221006115436.png]]

## Create Custom Views 

**Documentation** [Configure CTA Detail View Layouts](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/Configure_CTA_Detail_View_Layouts)

**From the Documentation**

>As you saw in the scenario above, users can create their own Views from Cockpit, but as the Gainsight Administrator, you may want to create some Custom Views for your organization, especially early in your deployment of Gainsight, to help drive adoption and alignment.
>
   **Note:** End Users cannot make changes to the admin defined custom views. However, they can make changes to the filters/columns of the admin defined view and save it as a new custom view.
>
You can create Custom Views for all users, or assign views only to specific users or user groups. For example, at Gainsight, our Education Services team has a specific Cockpit view for all of our upcoming training deliveries. This view is only available to members of the Education Services team because it is only relevant to us.

Views can be customized from the **Custom Views** section of the Call to Action page.

![[Pasted image 20221006120702.png]]

![[Pasted image 20221006120755.png]]

### Configure Tasks 
**Documentation** [Configure Cockpit Tasks](https://support.gainsight.com/Gainsight_NXT/04Cockpit_and_Playbooks/00Cockpit_Horizon_Experience/Admin_Guides/Configure_Cockpit_Tasks)

Tasks can be configured to display by due date or by playbook order. 

>**Task Display Order**
>
In the General Settings section, select whether tasks should be displayed in Playbook Order or Due Date Order.
>
**Playbook Order** will group Playbook tasks together, even if you create manual tasks with due dates that overlap the due dates of those tasks associated with the Playbook. 
>
**Due Date Order** will display the tasks in order of due date, regardless of their association with a Playbook.

The remainder of the configuration follows the same format as configuring CTAs. 

**Navigation** Administration -> Cockpit -> Tasks 


![[Pasted image 20221006131831.png]]


### Mass Edit CTAs and Tasks 

>**Mass Edit**
>
  The mass edit tool enables an admin to Reassign and Delete CTAs and Success Plans in bulk. For Tasks, it enables an admin to Reassign Ownership, Delete, and Edit the Priority or Status in bulk.

### Quiz 
1. **Q** Your organization recently implemented monthly CSM check-ins for Enterprise customers. As the Gainsight Admin, you should...
	1. **A** Create an automatic CTA called Monthly Check-In which will generate monthly for all Enterprise customers
2. **Q** You meet with a group of stakeholders to discuss the CTA Types that should exist in your org. After compiling a list of all suggestions, you have 40 CTA Types. You should...
	1. **A** Work with the team to reduce the number of CTA Types to only those which are most important for launch, with the plan to roll out more at a later date
3. **Q** True or False: Users can save a filtered list of CTAs as a new Custom View.
	1. **A** True
4. **Q** You can perform a Mass Edit on which of the following? Select all that apply.
	1. **A** Tasks
	2. **A** CTAs
5. **Q** True or False: Playbooks can be made inactive even if they are currently being used by existing CTAs.
	1. **True** 

![[Cockpit_and_Playbooks_-_Learner_Exercise.pdf]]

