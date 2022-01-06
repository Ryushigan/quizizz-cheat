# Quizizz-cheat

Script is made by "gbaranski".
I only customized this based on my own preferences.

## Fetching Quizizz API

Instructions:
1. Open quizizz and join any quiz
2. Open console, copy and paste this
```ts
fetch("https://raw.githubusercontent.com/Ryushigan/quizizz-cheat/master/dist/bundle.js")
.then((res) => res.text()
.then((t) => eval(t)))
```
3. "Run" the script given above on the console
4. The correct answers should be visible now, you can now close the console and continue your quiz



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
