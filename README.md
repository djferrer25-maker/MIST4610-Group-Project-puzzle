# MIST4610-Group-Project
This project is the creation of a complex data model for our class's data management group project. 

Group 2

Ian Martin
Daniel Ferrer
Noila Rahimjon
Oraa Raysoni
Sisira Gudi

PuzzleVerse is a new online store that creates and sells a wide variety of custom jigsaw puzzles. To keep our operations running smoothly, we need a database that can track our sales, our customers, and our product designs.
Here's what the database manages:

Customers: We need to keep a list of our Customers, including their names, emails, phone numbers, and their default shipping addresses.
Orders: When a customer places an Order, we need to track the order date, total cost, and its current status (like 'Processing' or 'Shipped').
Order Items: An order can have multiple puzzles, so we need to know which puzzles and the quantity of each are in any given order.
Products & Categories: Our Products (the puzzles) have a name, piece count (e.g., 500, 1000), and a price. To help customers shop, we also sort them into Categories like 'Sports', 'Animals', or 'Movies'. A single puzzle can belong to multiple categories.
Artists: Our designs are made by Artists. We need to track each artist's name, email, and their pay rate for each design. Each puzzle is made by one artist, but an artist can design many puzzles.
Custom Orders: We offer a 'Custom' puzzle service. When a customer submits a Custom_Order_Request, we must link it to that customer and to an Employee who approves it. Once approved, this request will generate a new, unique puzzle in our Products table.
