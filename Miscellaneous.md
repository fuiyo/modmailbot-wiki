## Listeners
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

## Plugins
*You should only use a plugin made by a trusted developers (from our [list of plugins](https://github.com/BotStudios/ModmailBot/Wiki/Plugins)) as they'll have access to your entire bot (e.g. Sending messages, reading threads, tokens, deleting threads)*
- **You will not be able to get support in our official support channel if you're using any third party plugins**
To add a plugin ([example](https://npmjs.com/example-modmail-plugin)):
```js
const utils = new (require('./manager'))(client, collection);
const examplePlugin = require('example-modmail-plugin');

examplePlugin(utils);
```
