ONLINE SPORTS WORLD GUI Application
Project Overview
This project is a GUI application for user account management and shopping using Python's Tkinter library. It includes functionalities for signing up, signing in, and verifying user credentials and then allow shopping. The project is structured with the following main components:

ManageUserAccount Class: Handles user data storage, retrieval, and validation.
Interface Class: Manages the GUI elements for signing up and signing in.
Errors Class: Contains static methods for validating user input.
ProductMenu Class: Imported from product_menu.py, used to display product-related information.
UpdateCart Class: Manages the cart operations, including adding and removing items and saving the cart to a file.
ViewCart Class: Handles displaying the cart items in a tabular format and provides options for checkout and continuing shopping.
Checkout Class: Manages the checkout process, including reading cart items, displaying them, and handling the purchase confirmation.

Class Descriptions

ManageUserAccount Class:

Purpose: Handles file operations related to user account information.
Methods:
__init__(self, filename="user_info.txt"): Initializes the class with the filename where user data is stored.
save_user(self, username, password, address, contact): Saves user details to the file.
user_exist(self, username): Checks if a username already exists in the file.
authenticate_user(self, username, password): Verifies if the provided credentials are valid.

Interface Class:

Purpose: Creates and manages the GUI for user signup and signin.
Methods:
__init__(self): Initializes the GUI elements and starts the main Tkinter loop.
display_image(self, file): Displays an image on the root window.
create_widgets_signup(self): Creates the widgets for the signup interface.
create_widgets_signin(self): Creates the widgets for the signin interface.
show_signin_window(self): Switches to the signin window.
signup(self): Handles the signup process.
signin(self): Handles the signin process.
on_focus_in(self, event): Handles the focus-in event for entry widgets.
on_focus_out(self, event): Handles the focus-out event for entry widgets.
show_product_menu(self, username): Creates and displays the ProductMenu window with the username.

Errors Class

Purpose: Validates user input.
Methods:
is_valid_username(username): Checks if the username is valid.
is_valid_password(password): Checks if the password is valid.
is_valid_address(address): Checks if the address is valid.
is_valid_contact(contact): Checks if the contact number is valid.
ProductMenu Class:

Purpose: Manages the product display and user interactions related to products.
Imported From: product_menu.py.

UpdateCart Class:

Purpose: Manages the cart operations, including adding and removing items and saving the cart to a file.
Methods:
__init__(self): Initializes the class with an empty cart.
product_list(self): Returns a list of available products with their prices.
increase(self, var, product): Increases the quantity of the specified product in the cart.
decrease(self, var, product): Decreases the quantity of the specified product in the cart.
save_cart(self): Saves the current cart items to temporary_cart.txt.

ViewCart Class:

Purpose: Handles displaying the cart items in a tabular format and provides options for checkout and continuing shopping.
Methods:
__init__(self, main_window, username): Initializes the class with the main window and username.
read_items_from_file(self): Reads the cart items from temporary_cart.txt.
show(self): Displays the cart items in a Tkinter window.
continue_shopping(self): Closes the cart view and shows the main product menu window.
checkout(self): Closes the cart view and initiates the checkout process.

Checkout Class:

Purpose: Manages the checkout process, including reading cart items, displaying them, and handling the purchase confirmation.
Methods:
__init__(self, username): Initializes the class with the given username and reads cart items from the file.
read_cart_items(self): Reads the cart items from temporary_cart.txt.
get_price(self, product_name): Returns the price of the given product name from a predefined dictionary of products and prices.
show_checkout(self): Creates and displays the checkout window with the list of cart items, total price, and payment method.
confirm_purchase(self): Saves the purchase details to a file and displays a thank you window.
display_thank_you_window(self): Displays a thank you window for 3 seconds and then exits the application.
