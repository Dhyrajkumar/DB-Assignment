**Question_1:- Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.**

**Answer:-** the "Product" and "Product_Category" entities have a relationship where a product can be associated with one product category, and each product category can have multiple products associated with it. This is denoted by the "category_id" field in the "Product" entity, which is a foreign key referencing the "id" field in the "Product_Category" entity. This arrangement allows for organizing and categorizing products efficiently, enabling better management and retrieval of product information based on their categories.




**Question_2:- How could you ensure that each product in the "Product" table has a valid category assigned to it?**

**Answer:-** To ensure that each product in the "Product" table has a valid category assigned to it, you could implement a constraint in the database schema that enforces a foreign key reference on the "category_id" field in the "Product" table to the "id" field in the "Product_Category" table. This would ensure that every value in the "category_id" field corresponds to a valid category in the "Product_Category" table.

Additionally, you could also implement validation logic in your application before saving or updating a product record. Verify that the provided category_id corresponds to an existing category in the "Product_Category" collection. If the category is invalid, prevent the operation and return an error message. This would provide an extra layer of validation beyond the database constraint.

