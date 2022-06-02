# Tooling

Kali is not mandatory to pwn the shop, but it's way more convenient. Lots of challenges require a specific tool to be solved in reasonable time. Otherwise, it can take a while!

Even if you have your favorite scanner or fuzzer, it's often more efficient to test other tools to find the right one, a.k.a. the one the maintainers of Juice Shop have in mind.

## Kali Linux

The super-charged hacking OS is handy. You need to install npm (it's not prepackaged):

```
sudo apt install npm
```

### Burp suite (built-in with Kali)

Burp can cover most moderate challenges (from 1 to 4 stars), including the Brute-Forcing. Just send the intercepted login request to the intruder's mode.

## ZAP

ZAP by OWASP can run analysis and quick scans, which may speed up the hack here siginificantly. It's not prepackaged in Kali like Burp, but it's easy to install.

## Python/pip/packages

* uncompyle6

## Exiftools

`sudo apt install exiftool`

## KeypassXC

On Kali, it's the best alternative to keepass2 to open the .kdbx file.

## Insomnia

As HTTP client.