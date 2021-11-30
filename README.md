[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

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


| Event | Description |
|-|-|
|**ready**|Automatically initialized once the client is ready|
|**join**|Triggered once the the [user object] joins a game|
|**question**|Triggered once a question is received 
| **end** | Called upon once the game has ended

All events are described in detail at the __documentation__[*needs-link*]

**Join Game Example:**
Basic Syntax: ``[client].join(gameid, username, bot=True)``
| Name | Description |
|-|-|
|**``gameid``**|The GameID of the game you want to connect to|
| **``username``** | Username of the player/bot
|**``bot``**|<ins>boolean</ins> (True/False)

**Flood Game Example:** <sup style="color:red">Dangerous</sup>
Basic Syntax: ``[client].flood(gameid, username, amount)``
| Name | Description |
|-|-|
|**``gameid``**|The GameID of the game you want to connect to|
| **``username``** | Username of the bots
| **``amount``**| Amount of bots that will flood the game
|**``bot``**|Automatically set as true, cannot be modified.
ⓘ **WARNING:** BlooketAPI will <ins>automatically</ins> add a random number ``[int]`` into the username.

Eg, if you decide to flood the game with *3* bots that has the username "Example" then it would look like this:

``Example`` (FIRST BOT)
``Example 2`` (SECOND BOT)
``Example 3`` (THIRD BOT)

**Question Event Properties:**
| Name | Description |
|-|-|
|**``question``**|The base of the question|
| **``question.info``** | Information about the question
|**``question.answer``**|Answer to the question

**Question Information Properties:**
- ``name`` [**Name of the question**]
- ``options`` [**Solutions of the question**] 

[contributors-shield]: https://img.shields.io/github/contributors/Blooket-API/BlooketJS.svg?style=for-the-badge
[contributors-url]: https://github.com/Blooket-API/BlooketJS/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Blooket-API/BlooketJS.svg?style=for-the-badge
[forks-url]: https://github.com/Blooket-API/BlooketJS/network/members
[stars-shield]: https://img.shields.io/github/stars/Blooket-API/BlooketJS.svg?style=for-the-badge
[stars-url]: https://github.com/Blooket-API/BlooketJS/stargazers
[issues-shield]: https://img.shields.io/github/issues/Blooket-API/BlooketJS.svg?style=for-the-badge
[issues-url]: https://github.com/Blooket-API/BlooketJS/issues
[license-shield]: https://img.shields.io/github/license/Blooket-API/BlooketJS.svg?style=for-the-badge
