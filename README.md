# MIST4610-Group-Project
This project is the creation of a complex data model for our class's data management group project. 

Group 2

Team Members:
[Daniel Ferrer](https://github.com/daniel-ferrer-maker)
Ian Martin 
Noila Rahimjon 
Oraa Raysoni 
Sisira Gudi

Problem Description:
The task at hand is to model and build a relational database for the general workings of an e-commerce company, "PuzzleVerse." The central goal is to track the company's product catalog, customer sales, and artist collaborations. The model must support all core business functions, from managing customer orders and payments to tracking product designs and custom requests.
We are interested in accurately modeling these relationships, generating sample data to populate the entities and their attributes, and formulating 10 functioning queries on this data to provide valuable business insights about PuzzleVerse's operations.

Data Model:
Our data model, "PuzzleVerse," is structured to support all facets of this custom puzzle business, using essential entities and their relationships to correctly support different areas of the business such as sales, product management, and customer relations.
First off, the Customers entity represents our customer base. Within this entity, we have the primary key (idCustomers), as well as the customer's name, email, and phone number. A customer can have multiple shipping addresses, so the Customers table is linked via a one-to-many relationship to the Addresses table, which stores the street, city, state, and zip for each address.
Customers place Orders, which forms a one-to-many relationship where one customer can have multiple orders. The Orders entity contains its own primary key (idOrders), a foreign key from Customers, and attributes such as the OrderDate, TotalCost, and Status. Each order is also linked to one or more Payments in a one-to-many relationship.
Since each order can consist of multiple products, we introduce the Order_Items table. This associative entity links Orders and Products in a many-to-many relationship. Within the Order_Items table is its own primary key (idOrder_Items), as well as two foreign keys pulled from the Orders and Products tables. It also tracks the quantity of each product and the UnitPriceAtSale to capture the price at the time of purchase.
The Products entity is central to our catalog. Each product has a primary key (idProducts), a name, piece count, and a standard unit price. Each product's artwork is designed by an Artist, forming a one-to-many relationship. The Artists table stores the artist's name, email, and pay rate. To allow for a rich product page, each product can also have multiple images, linking it to the Product_Images table. Furthermore, Products and Categories have a many-to-many relationship, joined by the Products_Categories table, allowing a puzzle to be listed under "Animals" and "Landscapes" simultaneously.
Finally, the Custom_Order_Requests entity manages our custom puzzle service. This table links a Customer and an Employee (who manages the request) to a potential Product. This entity tracks the approval status, image link, and description for each custom design.

Data Model: 
<img width="974" height="945" alt="project" src="https://github.com/user-attachments/assets/a0982940-b574-48a3-9fda-83483fc0e6ca" />
