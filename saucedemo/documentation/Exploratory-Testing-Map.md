# Exploratory Testing Map - [SauceDemo](https://www.saucedemo.com/)

## CHARTER

Exploring the key elements and behaviours of SauceDemo's pages and functions.
Verifying it's user flow and usability.

- **Test Users**: standard_user, locked_out_user, and problem_user
- **Password**: secret_sauce

## TEST IDEAS

## EXECUTION NOTES

| **Test User** | **Actions Performed**                                              | **Observed Behavior**                                                                 |
| ------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| standard_user | Entered username & password and click 'Login' button on Login Page | Successful login and redirected to Inverntory Page                                    |
| standard_user | Clicked on item on Inventory Page                                  | Redirected to item's detailed page                                                    |
| standard_user | Clicked 'Add' button on Inventory Page                             | Item was added to the cart, and the cart icon showed the item count increase by one   |
| standard_user | Clicked 'Remove' button on Inventory Page                          | Item was removed to the cart, and the cart icon showed the item count decrease by one |

## BUGS/ISSUES FOUND

| **Test User**   | **Actions Performed**                                              | **Observed Behavior**                                                                   |
| --------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| standard_user   | Completed checkout process with an empty cart                      | Checkout successfully completed, success message:'Thank you for your order!'            |
| locked_out_user | Entered username & password and click 'Login' button on Login Page | Login unsuccessful, error message:'Epic sadface: Sorry, this user has been locked out.' |
| problem_user    | Browsed Invertory Page                                             | Some items had incorrect names and descriptions, all items had incorrect images         |
| problem_user    | Clicked sorting by 'Name(Z to A)' on Inventory Page                | All items were not sorted in desecending alphabetical order                             |
| problem_user    | Clicked on inventory item on Inventory Page                        | Taken to an incorrect item's detail page                                                |
| problem_user    | Clicked on 'Remove' button on Inventory Page                       | Button was unfunctional, item remained in cart and cart icon did not decrease by one    |
| problem_user    | Entered user information on Checkout Step Two Page                 | Last Name field is not functional                                                       |

## QUESTION/RISKS/FOLLOW-UPS

Things that need investigation, clarification from developers, or deeper testing
later. Include blockers that stopped you from testing certain areas.

| **Questions/Risks** | **Clarification**                                                   |
| ----------------- | ------------------------------------------------------------------ |
| Multiple Items         | Completed checkout process with an empty cart                      |
|    | Entered username & password and click 'Login' button on Login Page |
