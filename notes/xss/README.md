# XSS

## Endpoints

I liked those challenges, as it's both simple and tricky to distinguish "reflected XSS" from the other XSS challenge (moderate diffulty):

* http://localhost:3000/#/track-result?id=%3Ciframe%20src%3D%22javascript:alert(%60xss%60)%22%3E
* http://localhost:3000/#/search?q=%3Ciframe%20src%253D%22javascript:alert(%60xss%60)%22%3E

## Tough challenges

I found those XSS challenges quite classic but still fun. "Perform a persisted XSS attack bypassing a client-side security mechanism" was the most difficult to unlock for me, but paradoxically the 3-stars challenge was more difficult than the 4-stars challenge with the same title.

## Bad CSP

> Content-Security-Policy img-src 'self' assets/public/images/uploads/defaultAdmin.png; script-src 'self' 'unsafe-eval' https://code.getmdl.io http://ajax.googleapis.com

The main difficulty was to beat the regex applied on the field called "username".