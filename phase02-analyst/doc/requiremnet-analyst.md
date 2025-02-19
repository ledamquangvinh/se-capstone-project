# Requirement Analyst

## 1 - Functional Requirement

### 1.1 - E-commerce Website

* The Homepage will be show the special product with:
    * Top 4 hot product.
    * Top 4 best-seller product.

* The Menu will show category of products.

* For each category, the system will display list of product which belong to the category.

* Product's Information will display at the Product Detail page.
* The user can sign up/sign in account in the system.
* To make a purchase, the user must be registered.
* After login with ***Customer*** account, the user can choose the products to shopping cart.
* The customer can manage the shopping cart with the items which haven't checkout. Optional, customer can make payment online via payment gateway.
* The customer can checkout the current shopping cart.
* The customer can check the status of their orders.

### 1.2 - Admin Dashboard

* After login with the Admin Role or Employee Role, the system will display the dashboard with the chart which visualize the summary of current reports about the selling in the system.

##### 1.2.1 - Employee Role:
* Manage the categories information.
* Manage the products information.
* Manage the orders information.

#### 1.2.2 - Admin Role:
* Manage User Account.
* Manage the system configuration.

## 2 - Non-functional Requirement
* Maximum loading Time is 3 seconds.
* The system must be security with authentication and authorization.

## 3 - User Role

List of user-role:
* ***Admin*** is the system manager. They only control the user's account and system configuration.

* ***Employee*** is the employee of the company. They will control the product information, process and orders,etc

* ***Customer*** is the online buyer. They have information and account in the system with role Customer. They can use customer account to make purchase on the online system.

* ***Guest*** is anonynous user. They can only view the product information in the system. They can register ***Customer*** account.