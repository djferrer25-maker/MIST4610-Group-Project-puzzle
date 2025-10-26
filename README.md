# MIST4610-Group-Project
This project is the creation of a complex data model for our class's data management group project. 

**Group 2**

Team Members:

[Daniel Ferrer](https://github.com/djferrer25-maker)

Ian Martin

Noila Rahimjon 

Oraa Raysoni 

Sisira Gudi

# Problem Description:

The task at hand is to model and build a relational database for the general workings of an e-commerce company, "PuzzleVerse." The central goal is to track the company's product catalog, customer sales, and artist collaborations. The model must support all core business functions, from managing customer orders and payments to tracking product designs and custom requests.
We are interested in accurately modeling these relationships, generating sample data to populate the entities and their attributes, and formulating 10 functioning queries on this data to provide valuable business insights about PuzzleVerse's operations.

# Data Model:

Our data model, "PuzzleVerse," is structured to support all facets of this custom puzzle business, using essential entities and their relationships to correctly support different areas of the business such as sales, product management, and customer relations.
First off, the Customers entity represents our customer base. Within this entity, we have the primary key (idCustomers), as well as the customer's name, email, and phone number. A customer can have multiple shipping addresses, so the Customers table is linked via a one-to-many relationship to the Addresses table, which stores the street, city, state, and zip for each address.
Customers place Orders, which forms a one-to-many relationship where one customer can have multiple orders. The Orders entity contains its own primary key (idOrders), a foreign key from Customers, and attributes such as the OrderDate, TotalCost, and Status. Each order is also linked to one or more Payments in a one-to-many relationship.
Since each order can consist of multiple products, we introduce the Order_Items table. This associative entity links Orders and Products in a many-to-many relationship. Within the Order_Items table is its own primary key (idOrder_Items), as well as two foreign keys pulled from the Orders and Products tables. It also tracks the quantity of each product and the UnitPriceAtSale to capture the price at the time of purchase.
The Products entity is central to our catalog. Each product has a primary key (idProducts), a name, piece count, and a standard unit price. Each product's artwork is designed by an Artist, forming a one-to-many relationship. The Artists table stores the artist's name, email, and pay rate. To allow for a rich product page, each product can also have multiple images, linking it to the Product_Images table. Furthermore, Products and Categories have a many-to-many relationship, joined by the Products_Categories table, allowing a puzzle to be listed under "Animals" and "Landscapes" simultaneously.
Finally, the Custom_Order_Requests entity manages our custom puzzle service. This table links a Customer and an Employee (who manages the request) to a potential Product. This entity tracks the approval status, image link, and description for each custom design.

# Data Model: 
<img width="974" height="945" alt="project" src="https://github.com/user-attachments/assets/a0982940-b574-48a3-9fda-83483fc0e6ca" />

# Data Dictionary: 

**Customers:**

<img width="896" height="193" alt="image" src="https://github.com/user-attachments/assets/3139354d-826e-4544-9183-17c6aa225dee" />

**Artists:**

<img width="686" height="145" alt="image" src="https://github.com/user-attachments/assets/3598c1a7-cf52-4b9e-b3c7-25c227604aa1" />

**Orders:**

<img width="831" height="169" alt="image" src="https://github.com/user-attachments/assets/fc69705b-3958-4eef-a0ab-de29866e7a01" />

**Adresses:**

<img width="754" height="193" alt="image" src="https://github.com/user-attachments/assets/57bee603-f9dc-4764-a076-8a09d8d5d744" />

**Products:**

<img width="891" height="217" alt="image" src="https://github.com/user-attachments/assets/99f50fd3-04b1-4ad8-91d0-f15e72fd1900" />

**Order Items:**

<img width="756" height="145" alt="image" src="https://github.com/user-attachments/assets/740389dc-d363-464c-9739-8a911d3dd265" />

**Payments:**

<img width="839" height="169" alt="image" src="https://github.com/user-attachments/assets/26e81efe-4533-49bd-b6ba-d2436f7b6a35" />

**Product Images:**

<img width="794" height="145" alt="image" src="https://github.com/user-attachments/assets/bb05b095-9e16-4456-a235-5187c9132034" />

**Product Categories:**

<img width="656" height="73" alt="image" src="https://github.com/user-attachments/assets/95e0f2ff-0926-4cbb-b5a5-ba277d382064" />

**Categories:**
		
<img width="678" height="97" alt="image" src="https://github.com/user-attachments/assets/32cb7537-bf74-49bd-8c02-0c9abfb394ee" />










