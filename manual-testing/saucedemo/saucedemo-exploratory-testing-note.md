# Exploratory Testing Note - SauceDemo
Here is a high level summary of the functions, user flows and behviours of the saucedemo web application.


- Website :[SauceDemo](https://www.saucedemo.com/)
- Test Users: standard_user, locked_out_user, problem_user, performance_glitch_user
- Password: secret_sauce

## Test User Behaviour

| Username                | Observed Behavior                                         |
| ----------------------- | --------------------------------------------------------- |
| standard_user           | Normal flow works                                         |
| locked_out_user         | Cannot login, shows error                                 |
| problem_user            | Missing images, cart issues, wrong inventory item details |
| performance_glitch_user | Slow pageload, buttons delayed                            |

## Happy Paths:

1. Login page -> Enter valid credentials -> Click Login -> Directed to Inventory page
2. Inventory page -> Browse Inventory -> Add/Remove item from cart -> Go to Cart page
3. Inventory page -> Click Inventory Item Card -> Inventory Item Page -> Add/Remove item from cart -> Go to Cart page
4. Cart Page -> Click Checkout -> Checkout Step One -> Enter accurate information -> Checkout Step Two -> Review & Confirm purchase -> Complete

