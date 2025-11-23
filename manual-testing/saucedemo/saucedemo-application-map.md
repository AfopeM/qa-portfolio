# Application Map - SauceDemo

Here is the breakdown of the navigational structure, pages and key elements of the Sauce Demo web application

## Column Descriptions:

- Page: The descriptive name of the page.
- URL: The relative path of the page.
- Key Elements: The most important buttons, links, fields, and text present on the page.
- Conntected To: Other pages accessible directly from this page.

## Page Navigation Breakdown:

| Page              | URL                         | Key Elements                                                                                          | Connected To                                                              |
| ----------------- | --------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Login             | /index.html                 | Username field, Password field, Login Button, Error Message                                           | Inventory (Login Button)                                                  |
| Inventory         | /inventory.html             | Sort Dropdown Menu, Inventory Item Card, Add Button, Remove Button                                    | Inventory Item (Inventory Item Card)                                      |
| Inventory Item    | /inventory-item.html?id=[#] | Name, Description, Image, Price of Inventory Item, Add Button, Remove Button, Back to Products Button | Inventory (Back to Products Button)                                       |
| Cart              | /cart.html                  | Continue Shopping Button, Checkout Button, Cart Item, Remove Button                                   | Inventory (Continue Shopping Button), Checkout Step One (Checkout Button) |
| Checkout Step One | /checkout-step-one.html     | Cancel Button, Continue Button, User Info Form, Error Message                                         | Cart (Cancel Button)                                                      |
| Checkout Step Two | /checkout-step-two.html     | Cart Item, Order Summary, Payment Summary, Cancel Button, Finish Button, Error Message                | Checkout Step One (Cancel Button), Checkout Step Complete (Finish Button) |
| Checkout Complete | /checkout-complete.html     | Back Home Button                                                                                      | Checkout Step Two (Back Home Button)                                      |

All pages inherit the Global Navigation elements listed below.

## Global Navigation:

| Key Elements                | Function                                                                  |
| --------------------------- | ------------------------------------------------------------------------- |
| All Items (Side Menu)       | Directs the user to the inventory page[/inventory.html]                   |
| About (Side Menu)           | An external link to the Sauce Lab's marketing page                        |
| Logout (Side Menu)          | The user is logged out and redirects them to the Login page[/index.html]  |
| Reset App State (Side Menu) | Clears cart and redirects the user to the inventory page[/inventory.html] |
| Cart Icon Button            | Directs the user to the Cart page[/cart.html]                             |

The footer menu contains external links to Sauce Lab's facebook, twitter, and linkedin social media pages.
