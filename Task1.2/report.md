# Shopping Cart Script Report

This report details the functions within the shopping cart script in `index.html`.

### `addToCart(productId)`

This function is called when a user clicks the "Add to Cart" button. It finds the corresponding product in the `products` array. If the product is already in the `cart`, it increases the quantity; otherwise, it adds the product to the cart with a quantity of 1. Finally, it calls `renderCart()` to update the UI.

### `removeFromCart(productId)`

This function removes an item from the cart entirely, regardless of its quantity. It filters the `cart` array to exclude the item with the specified `productId`. After removing the item, it calls `renderCart()` to reflect the changes in the shopping cart display.

### `updateQuantity(productId, change)`

This function adjusts the quantity of a product in the cart. It takes a `change` value, which can be `1` to increase or `-1` to decrease the quantity. If the quantity drops to zero or below, the item is automatically removed from the cart by calling `removeFromCart()`. Otherwise, it updates the cart display.

### `calculateTotal()`

This function computes the total cost of all items in the shopping cart. It iterates through the `cart` array, multiplying the price of each item by its quantity and summing up the results. The final total is then displayed in the cart summary, formatted to two decimal places.

### `renderProducts()`

This function is responsible for displaying the list of available products on the page. It dynamically creates the HTML for each product card from the `products` array and injects it into the products grid. This makes the product listing easy to manage and update.

### `renderCart()`

This function updates the entire shopping cart UI. It clears the current cart display and re-renders it based on the items in the `cart` array. It also updates the total number of items in the cart badge and calls `calculateTotal()` to refresh the total price.

### `toggleCart()`

This simple function controls the visibility of the shopping cart section. It checks the current display state of the cart and toggles it between `block` (visible) and `none` (hidden). This allows the user to show or hide the cart as needed.
