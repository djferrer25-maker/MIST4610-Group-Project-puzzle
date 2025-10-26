# MIST4610-Group-Project
This project is the creation of a complex data model for our class's data management group project. 

Group 2

Team Members:

Daniel Ferrer

Ian Martin

Noila Rahimjon

Oraa Raysoni

Sisira Gudi


Problem Description:
The task at hand is to model and build a relational database for the general workings of an e-commerce company, "PuzzleVerse." The central goal is to track the company's product catalog, customer sales, and artist collaborations. The model must support all core business functions, including tracking Customers and their associated Addresses, managing Orders and Payments, and handling the Products themselves. It must also manage the relationships between Products, the Artists who design them, and the Categories they belong to. Finally, the system must support a Custom_Order_Request workflow, linking Customers to Employees for approval and a new product. We are interested in accurately modeling these relationships, generating sample data to populate the database, and formulating 10 functioning queries on this data to provide valuable business insights.

Data Model:
Our data model, "PuzzleVerse," is structured to support all facets of this custom puzzle business.
The core of the model is the Customers entity, which stores customer contact information. A customer can have one or more Addresses, so a one-to-many relationship links the Customers table to the Addresses table.
Customers also place Orders, forming a one-to-many relationship where one customer can have many orders. The Orders entity contains details like the order date, total cost, and status. Each Order is linked to one or more Payments in a one-to-many relationship. To track which items are in an order, we use an associative entity, Order_Items. This table creates a many-to-many relationship between Orders and Products and includes the quantity and the unit price at the time of sale. The Products entity is central to the catalog. Each Product is designed by one Artist, forming a one-to-many relationship between Artists and Products. Each Product can also have multiple images, so it is linked to the Product_Images table in a one-to-many relationship. To allow for flexible sorting, Products and Categories have a many-to-many relationship, joined by the Products_Categories table. Finally, the Custom_Order_Requests entity connects a Customer and an Employee (who manages the request) to a potential Product. This entity stores the approval status and details of the custom design.

Data Model: 
<img width="974" height="945" alt="project" src="https://github.com/user-attachments/assets/a0982940-b574-48a3-9fda-83483fc0e6ca" />
