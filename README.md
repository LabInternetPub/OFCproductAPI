# Open Food Club: Products API REST

This API has all the information about the products for the Open Food Club (OFC). You have available the following GET calls
from the default http port (80):

* GET **/api/v1/products**            --> returns the complete information of all products
* GET **/api/vi/products/{id}**       --> returns the complete information of a single product with id
* GET **/api/v1/products/price**      --> returns the id and price of all products. Every call returns a different price
* GET **/api/v1/products/{id}/price** --> returns the id and price of a single products. Every call returns a different price
* GET **/api/v1/categories**          --> returns a list with the product categories

## How the OFC wants you to use it?

### Load products
You need to retrieve all the products from this API at least once in order to populate your database. The list of products
will not change. However, while you use the H2 database in memory, you may need to call it every time the application is run.

In order to save time, during development, you can use the sql files in the resources directory (schema.sql, and data.sql) to upload all the 
products from the disc and not from the API.

### Product price update
You need to update the products every day. You may want to call the api/v1/products/price in order to obtain them and update
the prices in the database

## Where is it located?

You'll be given a url where the API is located, but alternatively you can also clone this repository and run it locally