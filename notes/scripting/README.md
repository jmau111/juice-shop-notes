# Scripting

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

## Forgery

### Coupons

There's a list of outdated coupons in `/ftp` (another challenge). The coupon are encoded with `z85`.

_N.B: `z85` is also in `package.json.bak`_

There are online decoders for that. You get a general pattern: MONTH YEAR PERCENT (MMMYY-%). It's then possible to forge a custom coupon to pass an order and solve the challenge.
