# How data access policies and rules protect your data

Data Access Management > The Data Access Management page > How data access policies and rules protect your data

Policies and rules protect your data by controlling access to it and applying data de-identification techniques that mask sensitive data while maintaining the data's usefulness. In Data Access Management, you can create reusable policies based on user, usage, or metadata context. These policies execute automatically on an unlimited number of data access requests.

Data Access Management offers data de-identification policies, data filter policies, and data access control policies.

* You use data de-identification policies to define data protections to apply to data attributes to de-identify them for a given use case.
* You use data filter policies to filter access to rows within data assets.
* You use data access control policies to grant groups of users read, write, or delete access to tables or views in a source system. Data Access Management pushes these policies down into your cloud data platform, which enforces the policy directly.

You can reuse policies across different environments or for multiple data releases to ensure consistent treatment for the same data asset.

### How to de-identify data while maintaining its usefulness

Using data de-identification policies as an example, let's start by looking at the result you want to achieve and see how Data Access Management helps you achieve it.

Your goal is to de-identify data while still maintaining that data's usefulness. This is where Data Access Management's data protections come in. A data protection defines a data de-identification technique for Data Access Management to apply to a given data element in a data set to de-identify it, while still preserving utility.

However, you don't want Data Access Management to apply the same data de-identification techniques to every data element in every data asset regardless of the user, the type of data, and the usage context. You want these data de-identification techniques to be conditional on the usage context. You use rules to ensure that Data Access Management applies the relevant data de-identification techniques to the right data elements according to the conditions of the data access request.

Rules are the building blocks of policies. Rules are conditional based on attributes such as user, characteristics of the data, and the usage context. Rules also take actions specific to data classes and data protections.

While rules apply to specific conditions, you might need multiple rules to meet the needs of a broader use case. You need to group this set of rules into a policy that defines the use case for which Data Access Management should apply them.

Similarly, you group related data de-identification policies into precedence tiers.
