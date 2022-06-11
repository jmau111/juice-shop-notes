# Eggs

## Nested Easter Eggs

Juice Shop contains several easter eggs you have to decode. The nested one is the ultimate goal...

For this one, you get a base64-encoded string:

> L2d1ci9xcmlmL25lci9mYi9zaGFhbC9ndXJsL3V2cS9uYS9ybmZncmUvcnR0L2p2Z3V2YS9ndXIvcm5mZ3JlL3J0dA==

It gives:

```
/gur/qrif/ner/fb/shaal/gurl/uvq/na/rnfgre/rtt/jvguva/gur/rnfgre/rtt
```

However, you won't solve the challenge by going to the above URL. It needs to be decrypted. I really appreciated the several layers of encoding. CTFs rarely gives you such information for free.

You sometimes have to base64decode several times in a row to get the final string. Here, it's not the case, it's a rot13 cypher:

> /the/devs/are/so/funny/they/hid/an/easter/egg/within/the/easter/egg

https://github.com/l50/base64_rot13_decoder/blob/master/base64_rot13_decode.py

![](egg.jpg)