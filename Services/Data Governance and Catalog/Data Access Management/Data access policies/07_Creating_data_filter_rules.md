# Creating data filter rules

You create data filter rules to control access to rows or records of data.

1. Open a data filter policy and select the **Rules** tab.
2. Click the plus sign.
   The **Overview** tab appears.
3. Enter a name and a description for the rule.
   The following image shows the **Overview** tab:

   ![The image shows the Overview tab, which includes Name and Description fields and a Next button.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-03813414-50FD-4820-82EB-883474AD3035-low.png)

4. Click **Next**.
   The **Rule** tab appears. On this tab, you specify the conditions under which Data Access Management will deny access to data records (such as table rows).
5. In the **Conditions** section, click **New Row**.
   The following image shows the **Conditions** section of the **Rule** tab:

   ![The image shows the Conditions section of the Rule tab. The tab includes two conditions. One condition is User Group is any of HR Team. The other condition is Usage Context is any of Customer Analysis. A "New Row" button appears. "Back," "Save," and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-9FD697AB-E6CE-4FC4-AFA8-BD8331380421-low.png)

6. Select **Or** or **And** to determine whether only at least one condition must be true ("Or") or all conditions must be true ("And") for the rule to activate.
7. For each condition, select an attribute, an operator, and relevant values.
   Each attribute appears.
8. Select a contextual attribute, such as "User Group" or "Usage Context."
9. Select an operator, such as "is any of" or "is not any of."
10. Click **Add Value** to select the value of the contextual attribute.
11. Click **New Row** again to create another condition.
12. Continue this process until you have created all of the conditions necessary.
    You can now create filters for this rule.

## Creating filters for data filter rules

Once you create conditions for data filter rules, you then create filters.

1. In the **Filter** section of the **Rule** tab, click **New Row**.
   The following image shows the **Filter** section of the **Rule** tab:

   ![The image shows the Filter section of the Rule tab. The user has indicated that if the data element classification "Postal Code" is a string that is any of 123456 then deny access to records.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-1138C0D2-BA76-4CEC-86E2-F7B1C88BCD8A-low.png)

2. Click **Select Data Element Classification**.
   The **Select Data Element Classification** window appears.
   The following image shows the **Select Data Element Classification** window:

   ![The image shows the Select Data Element Classification window, which includes a search bar, a list of search results, and Select and Cancel buttons.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-F079976D-A3DC-4C60-A49C-AE07841AE8BC-low.png)

3. Enter search terms.
4. Click a result.
5. Click **Select** to return to the **Rule** tab.
6. Select a data type, such as string or integer.
   **Note:** If you use data filter rules that use dates and might be applied as part of data filter policies in an Access Policy transformation in Data Integration, Informatica recommends that you create two data filter rules: one with a date data type and one with a timestamp data type with the same values.
7. Select an operator.
8. Click **Add Value**.
   **Note:** If you enter a text string, it is case sensitive.
9. Click **Add Value** again to add more values.
10. Click **New Row** to select another data element classification.
11. Add the data element classification, data type, operator, and values as needed.
12. Continue this process until you have specified filters for the required data element classifications.
    Data Access Management denies access to a field if it meets any one of the filters.
13. Click **Save**.
    You need to publish the policy associated with this rule for this new rule to take effect.
