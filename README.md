[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

### In Developement
# BlooketJS 💻
BlooketJS is the first API Wrapper for Blooket — Built by Developers for Developers. 
Create Blooket Bots to automatically control your blooket games and possibly win them for you.
- Focused on Cache 

# Basic Example
```js
const { Client } = require("blooketjs");
const client = new Client({ token: process.env.token })

console.log("Joining blooket...");
client.join(000000, "example");

cliebt.on("Ready", () => {
  console.log("Ready!")
});

client.on("join", () => {
  console.log("I joined the Kahoot!");
});

client.on("question", question => {
  console.log("A new question has started, answering the first answer.");
  question.submit(question.answer[0])
});

client.on("end", () => {
  console.log("The quiz has ended.");
});
```
Docs coming soon!

[contributors-shield]: https://img.shields.io/github/contributors/Blooket-API/BlooketJS.svg?style=for-the-badge
[contributors-url]: https://github.com/Blooket-API/BlooketJS/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Blooket-API/BlooketJS.svg?style=for-the-badge
[forks-url]: https://github.com/Blooket-API/BlooketJS/network/members
[stars-shield]: https://img.shields.io/github/stars/Blooket-API/BlooketJS.svg?style=for-the-badge
[stars-url]: https://github.com/Blooket-API/BlooketJS/stargazers
[issues-shield]: https://img.shields.io/github/issues/Blooket-API/BlooketJS.svg?style=for-the-badge
[issues-url]: https://github.com/Blooket-API/BlooketJS/issues
[license-shield]: https://img.shields.io/github/license/Blooket-API/BlooketJS.svg?style=for-the-badge
