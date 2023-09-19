# Alert-Suppression
### Exercise 2: Alert suppression

When a single alert isn't interesting or relevant, you can manually dismiss it.
In the previous step, we used the dismiss option to manually dismiss a single alert. However, you can use the suppression rules feature to automatically dismiss similar alerts in the future.

1.	From Microsoft Defender for Cloud sidebar, select **Security alerts**.
2.	Select **High volume of operations in a Key Vault** alert and then click on **Take action**.
3.	Expend the Suppress similar alerts section and click on **Create Suppression Rule**.
4.	The new suppression rule pane opens, provide a rule name: *Testing-AutoDismiss-KV*.
5.	On the reason field, select Other and leave a comment: *Lab 6 exercise*.
6.	Set rule expiration to be tomorrow (just a day ahead). **Click Apply and wait 10 minutes for the new rule to be applied.**
7.	Validate your alert suppression rule:
    - From the top menu, click on the **Create sample alerts** button.
    - Select the **Key vaults** plan only.
    - Click **Create sample alerts**.
    - You should now see only the new Key Vaults alerts **excluding the High volume of operations in a Key Vault**.
    - To test your rule, click **Simulate**.
![image](https://github.com/Sismahil/Alert-Suppression/assets/121772702/7367f105-fa84-4a64-84c3-cca00c4007ed)
![image](https://github.com/Sismahil/Alert-Suppression/assets/121772702/2bf3330e-8f8b-455a-8c9b-91fe5dc4a799)




> Note, you can create suppression rules on a management group level by using a built-in policy definition named Deploy - Configure suppression rules for Microsoft Defender for Cloud alerts in Azure Policy. To suppress alerts at the subscription level, you can use the Azure portal or REST APIs.

1. You can change your existing suppression rules or create new ones: from the top menu, select **Suppression rules**. 
2. Click on the rule you have recently created: `Testing-AutoDismiss-KV`.
3.  Change the expiration to be a month ahead from the current date. Click **Apply**.
4.  View dismissed alerts: On the Security alerts main page, on the filters section, change the Status filter to show only **Dismissed** items.
5.  You should now expect to see only **1 dismissed alert**: High volume of operations in a Key Vault Sample alert.
