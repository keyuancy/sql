# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).
![image](https://github.com/user-attachments/assets/2e67ea10-066e-4794-ae8a-92e54992c2bd)


## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.
![image](https://github.com/user-attachments/assets/a6c54d3d-204a-4db5-a2a9-74d3c9ba389c)

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?
Customer addresses are crucial data points. When managing customer addresses, the primary considerations revolve around how to store this information for future use, such as billing and product delivery. 2 typically two approaches: an overwrite method (Type 1) and a historical retention method (Type 2).

-- Type 1 (Overwrite Method): In this architecture, if a customer changes their address, the new address simply replaces the old one in the database. This means we always have the current address, but we lose any historical data. This approach is straightforward and keeps the database clean, which might be ideal for situations where address changes are infrequent or where historical data isn’t critical.

-- Type 2 (Historical Retention Method): In contrast, Type 2 retains all historical addresses by creating a new record each time an address is updated. This allows the business to track changes over time, which can be beneficial for analyzing customer behavior or resolving issues related to past orders. However, this method can lead to a larger database and requires careful management of records to ensure accuracy.

_Hint, search type 1 vs type 2 slowly changing dimensions.

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
```
privacy implications refrence to gnificant privacy implications associated with storing customer addresses, especially in a Type 2 architecture. 

Data Retention: Retaining historical address data can pose risks if the data is not adequately protected. If the database is compromised, sensitive customer information may be exposed.

Regulatory Compliance: Depending on the jurisdiction, businesses may be required to comply with data protection regulations (e.g., GDPR, CCPA). This includes obligations for data minimization, where organizations should only retain personal data as long as necessary.

User Trust: Customers are often hesitant to share their addresses if they believe their data might be misused. Transparency about how their data is stored and used can help build trust, but it also requires businesses to be responsible stewards of this information.

Data Access Controls: It’s crucial to implement strict access controls to ensure that only authorized personnel can access and modify customer addresses, particularly in a historical context. This helps protect against unauthorized access and potential data breaches.



## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```After taking a closer look at the AdventureWorks schema, I noticed a couple of key differences compared to my own Entity-Relationship Diagram (ERD). This got me thinking about whether I should tweak anything in my design.
 - -Table Structure and Naming Conventions:

AdventureWorks: I admire how AdventureWorks uses clear and descriptive names for its tables, like SalesOrderHeader and Product. This clarity makes navigating the database feel much easier and more intuitive. Plus, they have dedicated tables for categories, which keeps everything organized.
My ERD: In my version, I opted for simpler names like Orders and Items, which might be a bit too vague. Looking back, I realize that not having a dedicated table for product categories has limited my schema’s clarity. It’s a reminder to be more thoughtful in my naming conventions.
Relationships and Cardinality:


My ERD: My ERD doesn't emphasize these relationships as clearly. I mentioned that customers place orders, but I didn’t highlight that one customer can have multiple orders. This lack of clarity could lead to confusion when interpreting the data.

Differences Between AdventureWorks Schema and My ERD
1. Table Structure and Naming Conventions
AdventureWorks: I really like how AdventureWorks uses clear and descriptive names for its tables, like SalesOrderHeader and Product. It makes everything feel organized and easy to understand. They also have separate tables for things like product categories, which helps keep things tidy.
My ERD: In my version, I went with simpler names like Orders and Items, which might make sense at first but can feel a bit vague. I didn’t create a dedicated table for product categories, which I now see could have helped clarify things.
2. Relationships and Cardinality
AdventureWorks: One thing that stands out in AdventureWorks is how clearly they define relationships and their cardinality. For example, a Customer can have multiple SalesOrders, which shows a one-to-many relationship. It’s straightforward and really helps in understanding how everything connects.

Adding Junction Tables: If I haven’t done this already, I’d definitely consider adding junction tables for any many-to-many relationships. For instance, creating a ProductCategory table like AdventureWorks could help organize my data better.
Your answer...
```My ERD: On the other hand, my ERD might not communicate these relationships as well. I mentioned that Customers place Orders, but I didn’t really emphasize that a customer can have multiple orders. This could lead to confusion about how the data interacts.
Changes I Would Consider
- -Reflecting on the AdventureWorks schema has inspired me to make a few changes to my ERD:

1.Better Naming Conventions: I want to adopt more descriptive names for my tables and columns, similar to AdventureWorks. It might take a bit of extra effort, but I believe it will make the database much more navigable for anyone using it.

2. Clearer Relationships: I see the need to be more explicit about the relationships in my ERD. Properly indicating whether a relationship is one-to-many or many-to-many would help eliminate any misunderstandings about how the entities interact.

3. Adding Junction Tables: If I haven’t already done so, I would definitely consider adding junction tables for any many-to-many relationships. Creating a ProductCategory table, like in AdventureWorks, would help me better organize my data and provide clearer insights into product classifications.


# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
