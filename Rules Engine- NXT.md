![Gainsight Study Table Of Contents](https://github.com/Zennewman/Gainsight-Resources/blob/c3d83243d188e278daf0994903579e35242dd580/README.md)

# Rules Engine- NXT

## How the Rules Engine Works 
The rules engine queries Gainsight objects, external objects such as data flowing in form Salesforce and S3 Buckets for relevant information and allows further processing and manipulation of the data once pulled. 

**The Rules Engine is how Gainsight collects, aggregates and transforms data** 
- Aggregate data for easy access 
- Create dynamic customer health scores 
- Alert CSM of customers that are at risk or trending in the wrong direction 
- Surface opportunities for expansion 
- Monitor usage data at the individual level to spot engaged and unengaged users 

[Data Management - MDA](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Data%20Management%20-%20MDA.md)
![MDA Data Architecture](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/lJzQ1Ymrv78GOoaz_eoQu3YLoGx-FDSrJ.png)


## Creating Rules 
1. **Create Rule** define it's Name, Type and whether is for Companies or Relationships
2. **Setup Rule** define the data the rule will act on. Data can be selected from an object or the MDA. Data can also be transformed at this step. 
	- Simple queries for data sets 
	- Transformations including returning aggregations and population statistics such as COUNT. Formula fields can also be created. 
	- Merge different data sets. 
	- Create pivot tables to yield summary statistics such as AVERAGE, SUM, MIN, MAX.
	- Data sets can be previewed before moving on to the next stage. 
3. **Setup action** This is where we define what will be done with the data set once it's pulled. 
	- Create CTAs, set Health Scores, Update related objects...
	- Multiple actions can be taken
	- Actions taken can be further filtered to a subset of the data set based on additional criteria
	- This stage is where unique identifiers for matching can be selected, i.e. Gainsight Id, SFDC Id, etc.
4. Schedule- define time and frequency for when the action will fire.  

**Navigation** Administration -> Rules Engine -> Create New Rule 

>[!Idea]
>Record a Loom video of creating a rule to better document the process


## From the Documentation 

---
### Gainsight Limitations

![Gainsight Limitations](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/Pasted%20image%2020221013112935.png)



## Interface 

Multiple list views can be created and customized for displaying rules. Columns can be adjusted and filters can be applied. Lists can also be reordered. 

Next to the Rule Lists tab is the Rule Chains tab. Rule Chains all rules to be strung together to insure correct order of execution 


## Rules Engine Best Practices
---
Gainsight suggests few recommendations for the admins during the configuration of rules to improve the performance of the rule, minimize the rule run time, and reduce rule failure probability. These suggestions also act as a reminder/guidance for the admins to configure accurate and efficient rules.

The following areas of rule configuration in which Gainsight recommends suggestions to the admins:

-   **Filters in Tasks:** This suggestion is displayed when no filters are added to the tasks. It is recommended to add the filters to fetch only the required data to improve the performance of a rule.
-   **Date Filters in Tasks:** This suggestion is displayed when no date filters are added when the rule is scheduled to run regularly. It is recommended to add a date filter for a rule to fetch only the latest data.
-   **Unused Tasks:** This suggestion is displayed when any data from the tasks is not used anywhere in the rule. Therefore, admins can delete those tasks without any impact to the rule configuration.

--- 

Rules should be limited in the scope of their query to what's needed in order to perform optimally. 

**Additional Best Practices** 

- Naming Conventions 
- Chain rules for structuring order of execution
- Test before deploying 
>Remember always to **test your rules** and **evaluate results** before deploying new rules. When using test data, select a “run date” for a time that has qualifying data. After testing completely, run the rule manually the first time before scheduling. Add your email to the “Email failures during scheduled run” when scheduling.
>
  Keep in mind that a test run does not test a rule's **actions**, it only tests the **query**, so it’s possible a test run will succeed, but an actual run will not depending on the rule's actions.
- Use date filters (later dates are always a greater value than earlier dates)
>[!Example]
>Find Customers whose renewal date is within the last 7 days. 
>Renewal Date between Day 0 and Day -7 

## Troubleshooting 
**From the Documentation**

---
Rules Engine contains several features to help you troubleshoot your rules. First, there are icons on the Rules Engine listing that indicate how the last attempt to run the rule went. If it's a green check, there was no problem.</br> 
![Green Check](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/RI9ozXrmHunbMwHx_qTz63oh0mFxr8TgE.png)

An orange triangle with an exclamation point indicates a partial failure; typically, this means that the rule itself was successful, but no data was found. Often, this is caused by null values.</br>
![Orange Caution](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/2PAUqdgOponUh98g_vfHOTemmFxXiLsu7.png)

Finally, a red circle with an exclamation mark is displayed if the rule completely failed. This typically indicates that the rule itself has a problem, and should be revisited.</br>
![Red Exclaimation](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/q_Lk-BaPxGP6eB3h_kT_3fn5c2UtCYZ4G.png)

--- 
 
### Rule Summary 

Additional information about the rule can be gained from the Rule Info section of the Rule Summary as showing below. 

![Rule Summary](https://github.com/Zennewman/Gainsight-Resources/blob/344533146e40189b69b4b54fb53aad1026d99eff/Resources/Pasted%20image%2020221013132422.png)

Additionally it's queries, transformations and actions can be reviewed using the tabs along the top of the Rule Summary as well as the execution history for that particular rule. 

### Email Summary 
While testing a rule, Gainsight will send a log of successes and errors in the rule via email. 

### Nulls 

>[!Attention]
>Nulls are defined different from other systems 

>In the Rules Engine you will encounter the concept of “Nulls,” the treatment of which can lead to partial rule failures.
>
  Partial failures are often caused by null records that fail to meet criteria. NULL indicates an “Unknown” value, not zero or blank. To find null records, checking the log records for messages where ‘field name’ = null. You can often exclude these records through Rule criteria. Note that Null checks currently work only on numeric field







## Resources

- [Rules Engine - Prerequisite Knowledge and Limitations](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/02Admin_Guides/Rules_Engine_-_Prerequisite_Knowledge_and_Limitations)
- [Rules Engine Overview](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/01About/Rules_Engine_Overview)
- [Getting Started With Rules Engine](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/02Admin_Guides/01Getting_Started_with_Rules_Engine)
- [SFDC Edition](https://support.gainsight.com/SFDC_Edition/Rules_Engine)
- [Create Tasks in Rules Engine](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/02Admin_Guides/02Rules_Engine_-_Task_Creation)
- [Set up Rule Action Types Overview](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Set_up_Rule_Action_Types_Overview)
	-   _[Call to Action (Create)](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Create_CTA_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Create_CTA_Action_Type")_
	-   _[Call to Action (Close)](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Close_CTA_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Close_CTA_Action_Type")_
	-   _[Load to Company](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Company_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Company_Action_Type")_
	-   _[Load to User](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_User_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_User_Action_Type")_
	-   _[Load to Gainsight Object](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Gainsight_Object_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Gainsight_Object_Action_Type")_
	-   _[Load to People](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_People_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_People_Action_Type")_
	-   _[Set Score 2.0](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Set_Score_2.0_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Set_Score_2.0_Action_Type")_
	-   _[Load to Relationship V2](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Relationship_V2_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Relationship_V2_Action_Type")_
	-   _[Load to SFDC Object](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Configure_Load_to_SFDC_Objects_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Configure_Load_to_SFDC_Objects_Action_Type")_
	-   _[Call External API](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Call_External_API_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Call_External_API_Action_type")_
	-   _[Load to PX](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_PX_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_PX_Action_Type")_
	-   _[Load to Survey](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Survey_Action_Type "Load to Survey Action Type")_
	-   _[Load to Scorecard History](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Scorecard_History_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Scorecard_History_Action_Type")_
	-   _[Load to Success Plans 2.0](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Success_Plans_2.0_Action_Type "https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Set_Up_Rule_Action_Types/Load_to_Success_Plans_2.0_Action_Type")_
- [Best Practices of Rules Engine](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/03Tutorials/Best_Practices_of_Rules_Engine)
- [Rules Engine Troubleshooting and FAQs](https://support.gainsight.com/Gainsight_NXT/03Rules_Engine/FAQs/Rules_Engine_Troubleshooting_and_FAQs)


## Quiz 
1. **Q** Rules Engine uses ______________  to search your data for specific information.
	1. **A** Query language
2. **Q** The purpose of the Rules Engine is to:
	1. **A** All of the above
3. **Q** The anatomy of a rule contains the following steps:
	1. **A** Create Rule, Set up Rule, Set up Action, and Schedule
4. **Q** Rules can do the following:
	1. **A** All of the above 
5. **Q** if Workbook = object, column = ?
	1. **A** Field
6. **Q** The default view which has rules in alphabetical order is:
	1. **A** List view
7. **Q** What are rule chains?
	1. **A** Rules executed one after another with a shared schedule
	2. **A** Groups of rules chained together 
8. **Q** Identifiers tell the Rules Engine how to find unique records.
	1. **A** True
9. **Q** Rules Engine Listing sorts rules:
	1. **A** Chronologically
10. **Q** You can do multiple actions in one rule.
	1. **A** True
11. **Q** Separating data loading actions from other actions is a good practice.
	1. **A** True
12. **Q** To receive an email with an Excel attachment showing the results of your Rule:
	1. **A** Add your email to the “Email failures during scheduled run” when scheduling
13. **Q** The green check symbol, orange triangle and the red circle with an exclamation mark,  indicate Successful run, Partial Success, and Full failure, respectively.
	1. **A** True
14. **Q** Partial failure:
	1. **A** All of the above
15. **Q** Which of the following statements is **false**?
	1. **A** In databases, Null is Zero (0)
16. **Q** When a rule goes wrong, these are some steps you can take to troubleshoot:
	1. **A** All of the above
17. **Q** The Rule Summary contains:
	1. **A** All of the above


