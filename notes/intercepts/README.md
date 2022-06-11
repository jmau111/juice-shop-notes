# Intercepts

Burp Community Edition is a great tool for Juice Shop.

## Baskets

There are various challenges that consist of intercepting requests with customers' baskets. The most challenging for me was "Manipulate Basket." Took me several sessions to figure it out.

### Manipulate Basket

Use the parameter `BasketId` twice in the same request.

### Place an order that makes you rich

I passed a negative amount for the order, for example, `-$9999`