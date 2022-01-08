## Listeners
*The following assumes basic knowledge about the library [discord.js](https://npmjs.com/discord.js) and event handling*
- List of [events](https://github.com/BotStudios/modmailbot/blob/main/info.json)
- [Things that you should be aware of](https://github.com/BotStudios/modmailbot/wiki/Faq#1-listenersevent-handling)
```js
... index.js
const utils = new (require('./manager'))(client, collection);

utils.on('logCreate', (user) => {
  var embed = new Discord.MessageEmbed()
     .setColor('RANDOM')
     .setTitle('Thread Created')
     .setDescription('The staff team will get back to you as soon as possible.')
     .setTimestamp();
   user.send({ embeds: [embed] })
})

utils.on('logDelete', (user, staff) => { 
  var embed = new Discord.MessageEmbed()
     .setColor('RANDOM')
     .setTitle('Thread Closed')
     .setDescription(`Thread closed by ${staff.username}`)
     .setTimestamp();
   user.send({ embeds: [embed] })
})
```

## Plugins
*You should only use a plugin by a trusted developers (from our [list of plugins](https://github.com/BotStudios/ModmailBot/Wiki/Plugins)) as they'll have access to your entire bot*