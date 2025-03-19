Before creating data access policies on the Data Access Management page, select which type of policy best fits each of your use cases.

You can create the following types of policies:

* Data access control policies grant groups of users read, write, or delete access to tables or views in a specific source system. Data Access Management pushes these policies into your cloud data platform. The data source enforces the policy directly.

Data access control policies best serve the following types of use cases:
- Provisioning data for analytics in native cloud data platforms using native access controls and tools where some groups only require read access to entire tables or views of data while other groups require write access

* Data filter policies restrict or limit which records Data Access Management delivers to users.

Data filter policies best serve the following types of use cases:
- Complying with data privacy regulations such as HIPAA, GDPR, or data transfer regulations by limiting which records users can access
- Provisioning data for analytics in which the analysts should have only access to some of the data

* Data de-identification policies transform data in ways that you specify to de-identify sensitive data. The de-identified data might be tokenized to maintain the original format, generalized to a common year or month, or truncated to keep only minimal contents visible, making it useful for analysis.

Data de-identification policies best serve the following types of use cases:
- Complying with data privacy regulations such as HIPAA or GDPR while still being able to use the de-identified data for analysis
- Provisioning data for analytics in which the analysts should not have access to raw, un-redacted data

### Example scenarios

The following are examples that illustrate which type of data access policy to use in different business scenarios.

The Operations team at your financial organization needs write access to any customer data in accordance with financial regulations. Your organization's anti-money laundering (AML) department needs read access to customer data to ensure that no customers are laundering money through your organization. All of your customer data is stored in a Snowflake source system. Data access control policies would best serve this use case because you can write policies that Data Access Management would push directly into your Snowflake instance. For tables containing customer data, the data access policies can grant write access to the Operations team while granting read access to the AML department.

You have customers in Western Europe and the Middle East. Your organization stores customer data in data centers in Dublin, Ireland and Riyadh, Saudi Arabia. Data filter policies would best serve this use case because you can write policies that ensure that European customer data is only accessed and processed within the European Union and Saudi Arabian customer data is only accessed and processed within Saudi Arabia. This prevents your organization from running afoul of data sovereignty regulations included in the GDPR and the PDPL.

The compliance department at your healthcare organization wants to perform analytics on patient data to determine what percentage of patients are overdue for more than one preventative health screening. The patient data includes patient ID numbers, contact information, and medical history. Data de-identification policies would best serve this use case because you can write policies that replace patient ID numbers with tokens, redact all contact information, and leave medical history untouched. Using the tokenized patient ID numbers, your compliance department can determine how many preventative health screenings each patient is overdue for without being able to identify any individual patient. This prevents your organization from running afoul of data privacy regulations such as HIPAA.
