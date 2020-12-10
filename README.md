# BoardGamesStore

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 10.1.0.

## Versions

- Visual Studio Code - 1.48.1
- Bootstrap - 4.5.2
- JQuery - 3.5.1
- Angular - 10.1.0
- rxjs - 6.6.0
- Typescript - 4.0.2

## Install all packages

Run `npm install` to generate all packages that the project depends on. 

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Project Structure

### /src/index.html

Home page for the Board Games Store

### /src/assets/data

JSON files for the Data Model:

##### cart.json

| Element       | Type        |Description                                     | 
| ------------- |:-----------:|:----------------------------------------------:| 
| items         | List        |List of Cart Entries                            |
| total         | Long        |Sum of all Cart Entries Product Quantities      |

##### cartEntry.json

| Element             | Type        |Description                             | 
| ------------------- |:-----------:|:--------------------------------------:| 
| productName         | String      |Name of the product to add to cart      |
| productQuantity     | Long        |Quantity of products to add to cart     |


##### products.json

| Element             | Type        |Description                  | 
| ------------------- |:-----------:|:---------------------------:| 
| productName         | String      |Name of the product          |
| productDescription  | String      |Description for the product  |
| imageURL            | String      |URL for the product image    |
| stockQuantity       | Long        |Product quantity in stock    |

### /src/assets/images

Contains all the images for the products.

### /src/app/app.module.ts

Includes all the dependencies for the Board Games Store application. Is used to define the needed modules to be imported, the components to be declared and the main component to be bootstrapped.

### /src/app/app.component.ts

Includes the view logic behind the app.component.html.

### /src/app/app.component.html

This file contains the html file related to app component and is where the child components are rendered.

### /src/app/store/store.module.ts

Includes the child components dependencies for the Board Games Store application.

### /src/app/store/cart/cart.component.css

Includes the styles for the cart component.

### /src/app/store/cart/cart.component.html

Contains the html file related to the cart component.

### /src/app/store/cart/cart.component.ts

Includes the view logic behind the cart.component.html.

### /src/app/store/product/product-list/product-list.component.css

Includes the styles for the product-list component.

### /src/app/store/product/product-list/product-list.component.html

Contains the html file related to the product-list component.

### /src/app/store/product/product-list/product-list.component.ts

Includes the view logic behind the product-list.component.html.

### /src/app/store/store-data/store-data.service.ts

Service that includes the import of the data from the json files.
Contains the functions to process the data (add and remove product to cart, and update cart and cart entries).

## Functionalities

### Add Product to cart

- When the "plus" button is clicked the selected product is added to the cart.
- The cart items value is incremented by 1 and the stock level for the selected product is reduced by 1. 
- When the stock level of a product is 0 it is not possible to add more to the cart.


### Remove Product from cart

- When the "minus" button is pressed the product is removed from the cart.
- The cart items values is decreased by 1 and the stock level for the selected product is increased by 1.
- This functionality only works if a product was added to the cart before, this means that if a product was not added to the cart it will not be possible to remove it from the cart.


