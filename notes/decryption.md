# Decryption

## Eggs

### Nested Easter Eggs

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

## Encrypted announcement

This one requires coding. You have to use Null Byte poison to get the `encrypt.pyc` file, uncompile it and reverse the algorithm inside:

```Python
confidential_document = open('announcement.md', 'r')
N = 145906768007583323230186939349070635292401872375357164399581871019873438799005358938369571402670149802121818086292467422828157022922076746906543401224889672472407926969987100581290103199317858753663710862357656510507883714297115637342788911463535102712032765166518411726859837988672111837205085526346618740053
e = 65537
encrypted_document = open('announcement_encrypted.md', 'w')
for char in confidential_document.read():
    encrypted_document.write(str(pow(ord(char), e, N)) + '\n')

encrypted_document.close()
```

Then it's possible to reverse the operation as the original algorithm gives us hints to write the decryptor:

* the encrypted file will be the input for the script
* keys used to encrypt the message are hardcoded

_N.B: The script was not trivial to reverse, though, but it reminds challenges you can find in the first questions of Project Euler_