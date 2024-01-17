Stage 1/5: Read the ERD 
Description
Сreate a database to store manufacturers, products, sales, customers, employees, and inventory data. With that goal in mind, we will create tables with the appropriate relations, attributes, and data types for our car dealership. 
Objectives
Kindly review the entity-relationship diagram (ERD) for our sales database provided below:
 
The manufacturers table contains the information about manufacturers of cars in our dealership. The attributes of this table are the manufacturer_id, name, and country.
The products table contains information describing the cars in our dealership. You can view information such as the car model, price, horsepower, and fuel_efficiency. Customers want the best deals, and this information helps them decide. 
You can find the current car inventory information on the inventory table; information on car sales is on the sales table. Information about our customers and employees is stored in the customers and employees tables respectively.
Your task is to create the manufacturers, products, and inventory tables with the ERD's required attributes, data types, and relations. 
Take note of the following:
•	There is a one-to-many identifying relationship between the products and inventory tables.
•	The product_id attribute in the inventory table is a FOREIGN KEY referenced to the products table.
•	The TINYINT datatype stores boolean values where 0 represents false, and 1 represents true.
•	Restrict the attributes of all the tables to NOT NULL except for attributes set as PRIMARY KEY.
•	AUTO_INCREMENT the attributes set as PRIMARY KEYexcept in the inventory table.
•	The dealership reorders a car from the manufacturer when the inventory quantity drops to two cars.
Stage 2/5: Pull the trigger 
Description
In the previous stage, you have shown your ability to create tables and establish relationships by analyzing the ERD. To avoid redundancy, we have prepared all the tables and their corresponding relationships in this stage.
We currently have agreements with Toyota and General Motors (GM) car makes. Our inventory comprises the Camry and Corolla models for Toyota and Silverado and Camaro for GM. These car models are among the most highly demanded vehicles in our locality.
To maintain precise records of our car sales and inventory, we must constantly update the inventory table whenever a deal is made. While it is possible to update the sales table first and then the inventory table, this approach has the potential for errors, as there is a risk of forgetting to update one of these tables. Consequently, if we stock our inventory, our records may not balance properly.
Stage 3/5: I like the view 
Description
Since the opening of the car dealership, the sales team has performed impressively, and in anticipation of increased sales, the sales manager has hired a new sales associate. Recently, the team has sold more cars, and as a result, the sales manager is interested in optimizing the product mix of the dealership. The sales manager requires data on the number of cars sold for each brand to achieve this.
As our database grows, the time to execute the query that outputs this information to the sales manager increases. The sales manager also finds it frustrating to connect the tables required to get this information over the ERD. Since it is a query the sales manager runs very often, the manager would like this process to be simplified.
Objectives
1.	Create the composite index, customer_sales_product, which will speed up the query execution
2.	Create a view, sales_summary, which outputs the model and total_sold attributes
3.	Run the sales_summary view to output its table
4.	Stage 4/5: Bonus points 
Description
The sales manager is satisfied with sales; 24 were sold in the last couple of days. To appreciate the commitment, the manager intends to implement a sales incentive program based on the total sales of each associate in comparison to the total sales for the month:
percent_revenue	employee_bonus
Less than 5	0
5 - 10	2,000
10 - 20	5,000
20 - 30	10,000
30 - 40	15,000
Greater than 40	25,000
Objectives
1.	Generate a table that shows the employee_name, position, month_year, and employee_bonus.
2.	Stage 5/5: Choose carefully 
Description
The car dealership is a capital-intensive business requiring substantial inventory investment. The sales manager can use this knowledge to make definable choices regarding the quantities of cars to carry for each car model and the level at which to restock them. Following the implementation of the sales incentive program, the sales manager wants to continue the innovations to secure the product mix and maximize profits.
Suppose we have equivalent profit margins for each car model and similar levels of customer satisfaction. In this scenario, the sales manager intends to use the sales inventory ratio to determine which car models to select. The sales inventory ratio is calculated by dividing the total sales per car model by its corresponding inventory. The manager will raise the percentage of models with a high sales inventory ratio and their reorder level.
Objectives
Generate a table that shows the model, price, total_sales_per_model, inventory_per_model, and sales_inventory_ratio

