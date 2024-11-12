This code defines an Inventory Management System (IMS) with features that allow different types of users (admin and regular users) to interact with an inventory of products. 
components and functionality:
 1. **Product Class**
   - Represents an individual product with attributes:
     - `product_id`, `name`, `category`, `price`, and `stock_quantity`.
   - Includes a method to adjust stock (`adjust_stock`) and a `__str__` method to display product information.

 2. **InventoryManagementSystem Class**
   - Manages the collection of products and handles user authentication, distinguishing between admin and regular users.
   - **User Authentication (`login` Method)**:
     - Checks username and password against predefined credentials and returns the user role.

   - **Admin-Specific Functions**:
     - **Add Product (`add_product`)**: Adds a new product if the product ID is unique.
     - **Edit Product (`edit_product`)**: Allows editing of specific attributes for a product.
     - **Delete Product (`delete_product`)**: Removes a product by ID.
     - **View Inventory (`view_inventory`)**: Lists all products in the inventory.
     - **Search Product (`search_product`)**: Searches by name or category.
     - **Check Stock Levels (`check_stock_levels`)**: Lists products with stock at or below a threshold.
     - **Adjust Stock (`adjust_stock`)**: Changes stock quantity for a specified product.

   - **Menus for Admin and User**:
     - **Admin Menu**: Options to view, add, edit, delete, check stock levels, adjust stock, and log out.
     - **User Menu**: Options to view the inventory, search products, and log out.

   - **Main System Execution (`run` Method)**:
     - Runs the IMS, prompting the user to log in and granting access to the appropriate menu based on their role.

This design allows:
- **Admins** to manage inventory fully, including adding, editing, deleting, and adjusting stock.
- **Regular Users** to view inventory and search for products.

You can start the system by initializing an instance (`ims = InventoryManagementSystem()`) and calling `ims.run()`, where users will be prompted to log in and proceed based on their role.
