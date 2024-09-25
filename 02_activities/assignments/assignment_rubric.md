# Assignment 1: Design a Logical Model Rubric

## General
  - Criteria: Participant Name on Assignment
  - Criteria: Written content is no longer than two pages
  - Criteria: Assignment is free of noticeable typos
  - Criteria: Two ERDs exist

## Question 1

  - **Tables**
    - Employee: Relates to employees.
    - Order: Relates to order processing.
    - Sales: Relates to sales transactions.
    - Customer: Relates to customer information.
    - Book: Relates to inventory of books.
![image](https://github.com/user-attachments/assets/7aa348dd-aad8-46e5-97b9-eccf7570bcb7)


  - **Tables Exist**: All five tables need to exist.
  - **Column Relevance**: Each table must have named columns that relate to their respective entities and include columns relevant for bookstore administration. (**🚨EACH table will be graded as complete or incomplete🚨**)
  - **Relationships Indicated**: Clear relationships between the aforementioned tables must be established.
  - **Date Table**: 
    - Must exist with typical columns.
    - Must have correct relationships with other relevant tables indicated.

## Question 2
- Employee Shift Table exists, and we can discern morning/evening shifts from its design**
![image](https://github.com/user-attachments/assets/5a38cee7-d2a5-46ab-95bb-95dad3d02dd5)

## Question 3: 
- **Two distinct architectures are proposed**
- **One design for Customer Addresses table would retain changes**
- **One design for Customer Addresses table would overwrite changes**
- **Each architecture is properly labelled as either Type 1 or Type 2 SCD**
    - Both Correct (Complete)
    - One Wrong (Incomplete)
    - Both Wrong (Incomplete)
 
  --Type 1 SCD (overwrites old address):**One design for Customer Addresses table would overwrite changes**

![image](https://github.com/user-attachments/assets/42607615-b93d-45e7-a976-a57bc86a0807)


-- Type 2 One design for Customer Addresses table would retain changes**
![image](https://github.com/user-attachments/assets/4bfb6460-a67e-46f3-b66c-5d47e920d530)



  

## Question 4: 
- **AdventureWorks ERD has been examined**
- **Two interesting differences between participant ERDs and AdventureWorks ERDs highlighted**
- **Student reflection on differences between the ERDs**

-- In my analysis of the AdventureWorks ERD, I found it to be a robust representation of a comprehensive business model. The AdventureWorks database encompasses various entities related to sales, production, and customer management, making it an excellent example of how a real-world business can be modeled in a relational database. The detailed relationships between entities, such as Customers, Orders, and Employees, demonstrate a complex interplay that accurately reflects the operations of a larger organization. This complexity helps in understanding the multifaceted nature of business processes and provides a solid foundation for building effective database systems.


Comparing the AdventureWorks ERD to my participant ERDs, two key differences stood out to me. First, the AdventureWorks ERD showcases a higher level of complexity and scope, integrating multiple business functions into a single model. In contrast, my participant ERDs focus on specific aspects of a system, often resulting in a simpler design. This simplicity can be beneficial for educational purposes or smaller applications, where clarity is paramount. Secondly, I observed differences in normalization practices. The AdventureWorks ERD emphasizes normalization to minimize redundancy, which is crucial for maintaining data integrity. My participant ERDs, however, might not adhere as strictly to normalization principles, sometimes prioritizing ease of use and development speed over strict data organization.


Reflecting on these differences has deepened my understanding of database design principles. The AdventureWorks ERD illustrates the importance of thorough planning and consideration of various business functions when creating a database model. It challenges me to think critically about how to effectively structure entities and their relationships in a way that captures the operational reality of a business. On the other hand, the participant ERDs remind me that simplicity and accessibility are vital, especially when communicating concepts to stakeholders or for learning purposes. Striking the right balance between complexity and usability is crucial, and this experience has equipped me with a better appreciation for the diverse approaches to designing effective database systems.

## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Question 1 Requirements|All requirements are met.|At least one requirement is not met.|
|Question 2 Requirements|All requirements are met.|At least one requirement is not met.|
|Question 3 Requirements|All requirements are met.|At least one requirement is not met.|
|Question 4 Requirements|All requirements are met.|At least one requirement is not met.|
