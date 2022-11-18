# Listeners
*The following assumes basic knowledge about the library [discord.js](https://npmjs.com/discord.js) and event handling*
- List of [events](https://github.com/BotStudios/modmailbot/blob/main/info.json)
- [Things that you should be aware of](https://github.com/BotStudios/modmailbot/wiki/Faq#1-listenersevent-handling)
```js
... index.js
const utils = new (require('./manager'))(client, collection);

utils.on('threadCreate', (user) => {
  var embed = new Discord.MessageEmbed()
     .setColor('RANDOM')
     .setTitle('Thread Created')
     .setDescription('The staff team will get back to you as soon as possible.')
     .setTimestamp();
   user.send({ embeds: [embed] })
})

utils.on('threadClose', (user, staff) => { 
  var embed = new Discord.MessageEmbed()
     .setColor('RANDOM')
     .setTitle('Thread Closed')
     .setDescription(`Thread closed by ${staff.username}`)
     .setTimestamp();
   user.send({ embeds: [embed] })
})
```

# Plugins
*You should only use a plugin made by trusted developers (from our [list of plugins](https://github.com/BotStudios/ModmailBot/Wiki/Plugins)) as they'll have access to your entire bot (e.g. Sending messages, reading threads, tokens, deleting threads)*
- **You will not be able to get support in our official support channel if you're using any third party plugins，however, you can still report your issue in the #third-party-plugins channel**

To add a plugin ([example](https://npmjs.com/example-modmail-plugin)):
```js
const utils = new (require('./manager'))(client, collection);
const examplePlugin = require('example-modmail-plugin');

examplePlugin(utils);
```

# Custom Commands

It is possible to implement a custom command for your modmail bot !

### Notes
- Implementing your own commands that are not officially verified by the developers may break the bot, implement a command at your own risk.
- We don't give support for custom commands
- You should only implement a command from a developer that you trust, the command modules are given access to your entire bot, this includes your token, and some serious data.
- Only the modmail staff (users with the modmail role) are able to execute these commands

### Module
Your command module should look like so
```
module.exports = {
    name: 'ping', // command name (required)
    description: 'Reply with pong', // description for this command, for the help command (required)
    run: async ({ message }) => { // function that will be executed when the command is triggered.
      message.reply("PONG");
    }
}
```

### Options
Functions that are available to command modules

| Key     | Description          |
| ------- | ------------------------------------------------------------------------------- |
| **bot** | The `client`, `utils` & `manager` objects (basically access to your entire bot) |
| **config** | Your config file |
| **message** | The message content |
| **args** | Arguments of the command |

