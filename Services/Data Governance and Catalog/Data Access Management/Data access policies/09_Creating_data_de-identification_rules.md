To define data de-identification rules, you add conditions based on user, usage, or metadata context, then assign data protections to data classes. Note that you must create data protections separately on the Data Protection tab in order to complete all steps in this procedure.

1. Open a data de-identification policy and select the **Rules** tab.

2. Click the plus sign.

   The **Overview** tab appears.

   The following image shows the **Overview** tab:

   ![The image shows the Overview tab, which includes Name and Description fields. "Next" and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-209465BE-8D2C-4351-BCFD-A18D4CB8E137-low.png)

3. Enter a name and description for the rule.

4. Click **Next**.

   The **Rule** tab appears. On this tab, you specify the conditions that will prompt Data Access Management to apply your data protections to data classes. You also specify the data protections.

5. In the **Conditions** section, click **New Row**.

   The following image shows the **Conditions** section of the **Rule** tab:

   ![The image shows the Conditions section of the Rule tab. The tab includes one condition. The condition is Usage Context is any of Customer Analysis. A "New Row" button appears. "Back," "Save," and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-4DD9571C-7312-47B4-980D-078680407FF5-low.png)

6. Select **Or** or **And** to determine whether only at least one condition must be true ("Or") or all conditions must be true ("And") for the rule to activate.

7. For each condition, select an attribute, an operator, and relevant values.

   Each attribute appears.

8. Select a contextual attribute, such as "User Group" or "Usage Context."

9. Select an operator, such as "is any of" or "is not any of."

10. Click **Add Value** to select the value of the contextual attribute.

11. Once you've selected the desired values within the list, click **Add Value** in the list to save those selections.

12. Click **New Row** again to create another condition.

13. Continue this process until you have created all of the conditions necessary.

    You now create field level de-identifications for this rule.

    The following image shows the **Field Level De-identification** section of the **Rule** tab:

    ![The image shows the Field Level De-identification section of the Rule tab. The user is working in the Field-Level Data Protections section of the page. The de-identification has a class of "Address Information," protected with a protection technique called "ConsistentToken."](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-A918A1CE-0D11-4E35-92DA-2831A928B29A-low.png)

14. Select a data class.

15. Assign a data protection to the data class.

    **Note:** You must have created a data protection separately on the Data Protection tab prior to this step in order to assign it in this step.

16. Click **New Row** to select another data class.

    Continue this process until you have specified all field-level data protections relevant to the rule.

17. Click **Save**.

    You need to publish the policy associated with this rule for this new rule to take effect.
