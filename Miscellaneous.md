## Listeners
*The following assumes basic knowledge about the library [discord.js](https://npmjs.com/discord.js) and event handling*
- List of [events](https://github.com/BotStudios/modmailbot/blob/main/info.json)
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