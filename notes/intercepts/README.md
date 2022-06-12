# Intercepts

Burp Community Edition is a great tool for Juice Shop.

## Baskets

There are various challenges that consist of intercepting requests with customers' baskets. The most challenging for me was "Manipulate Basket." Took me several sessions to figure it out.

### Manipulate Basket

Use the parameter `BasketId` twice in the same request.

### Place an order that makes you rich

I passed a negative amount for the order, for example, `-$9999`

## Change Bender's password into slurmCl4ssic 

It's neither an SQL Injection nor the Forgot Password. Indeed, the answer is in the instructions:

> change password

The app uses a pretty insecure API to change passwords that looks like the following:

> /rest/user/change-password/?current=xxxxxxx&new=wololo&repeat=wololo

It's even more flawed, as you can simply remove the `current` parameter to set whatever password you want:

> /rest/user/change-password/?new=slurmCl4ssic&repeat=slurmCl4ssic