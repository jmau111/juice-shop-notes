# OSINT

## Uvogin' security answer

> y0ur f1r3wall needs m0r3 musc13

=> uv0gin
=> https://twitter.com/uv0gin/status/1246167286924210176
=> https://web.archive.org/web/20200403193744/https://twitter.com/uv0gin

> Just watched Silence of the Lambs for the 18th time and it's still just as amazing as the first.
Sir Anthony Hopkins is the all-time best and there's no denying it

## Bender' security anwser

> America's most important brand of suicide booths is Stop'n'Drop

https://futurama.fandom.com/wiki/Suicide_Booth

## Morty

It's either "Snowball" or "Snuffles" (see wiki for Rick & Morty on Internet).

We get more info in additional hints:

> less than 10 chars

Both terms respect that condition. Like in other challenges, the password is probably tweaked to make it harder to guess. For example, a "3" for a "e", a "0" for a "o", a "4" for a "a", and so on.

The best approach is to build your own custom wordlist with different variations for each terms:

* numbers for letters
* uppercases and lowercases
* all combined

Once you have that wordlist, you can add a "pause" of 2s in your script to prevent any 429 error.

At least, _it worked for me_, and it was not a big deal, as the list is pretty short.
