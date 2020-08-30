# [Insta.js](https://npmjs.com/@androz2091/insta.js)

💬 Object-oriented library for sending and receiving messages via Instagram! Based on **[instagram-private-api](https://github.com/dilame/instagram-private-api)**, it is very similiar to **[discord.js](https://npmjs.com/discord.js)**.

## Example

Here is a simple chatbot made with the library:

```js
const Insta = require('@androz2091/insta.js');

const client = new Insta.Client();

client.on('connected', () => {
    console.log(`Logged in as ${client.user.username}`);
});

client.on('messageCreate', (message) => {
    if (message.author.id === client.user.id) return

    message.markSeen();

    if (message.content === '!ping') {
        message.reply('!pong');
    }
});

client.login('username', 'password');
```

## Links

* [Website](https://insta.js.org)
* [Documentation](https://insta.js.org/#/docs)
* [Insta.js Discord server](https://discord.gg/hw87VUQ)
* [GitHub](https://github.com/Androz2091/insta.js)
* [NPM](https://www.npmjs.com/@androz2091/insta.js)

## Credits

🧡 Big thanks to **[Nerixyz](https://github.com/Nerixyz)** and **[dilame](https://github.com/dilame)** for their libraries.
