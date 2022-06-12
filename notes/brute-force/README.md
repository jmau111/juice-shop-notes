# Brute Force

## Admin's password

You need/can use Brute Force to retrieve the admin password (challenge with 2 stars). It's quite straightforward as long as you **use the right wordlist**.

Otherwise, it will take like forever.

## Typosquatting

### Legacy

Once you get the package.json.bak file with the null byte attack, you can read the list of node dependencies.

There are more subtle ways to find the typosquatter, but I decided to enter all packages in the textarea on the contact page to solve the challenge.

Note that if you copy/paste the entire package.json file inside the textarea, it does not work because of the quotes and brackets. However, extracting names and versions from "dependencies"/"devDependencies" and send it as comment unlocks the challenge.

_N.B.: This "technique" cannot be used everywhere, for example, it does not work for the challenge that involves dangerous ingredients of a deleted product. You probably miss the point here, as it's about identifying a vulnerable package, but if you feel lazy on this one like me, you can use this trick_
