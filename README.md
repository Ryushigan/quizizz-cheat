# Quizizz-cheat

There are 2 methods for retrieving answers.

1. [Fetching Quizizz API](#fetching-quizizz-api)
2. [Sending answers as someone else](#sending-answers-as-someone-else) (old method)

You can load this script automatically using a browser extension.
- [Using Tampermonkey](#load-automatically-using-tampermonkey)

# Methods
## Fetching Quizizz API

It should work in Test and Classic mode.
1. Join Quiz
2. Open console and paste this
```ts
fetch("https://raw.githubusercontent.com/Ryushigan/quizizz-cheat/master/dist/bundle.js")
.then((res) => res.text()
.then((t) => eval(t)))
```
3. You can now close the console. The good answers should be highlighted by background opacity.

## Sending answers as someone else

An alternative method is more invasive. Instead of fetching Quizizz API, it sends a random answer to a current question as a different user (consuming his answer); as a response, Quizizz returns a valid answer, which is then displayed to the user.

1. Join quiz, wait for first question, and open console
2. Paste this code to the console
```ts
fetch("https://raw.githubusercontent.com/Ryushigan/quizizz-cheat/oldmethod/dist/bundle.js")
.then((res) => res.text()
.then((t) => eval(t)))
```
3. Enter the user name of any other player (the user won't get points even if they sent a valid answer).
4. Go to step 2