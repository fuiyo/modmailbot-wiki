It is possible to implement a custom command for your modmail bot !

## Notes
- Implementing your own commands that are not officially verified by the developers may break the bot, implement a command at your own risk.
- We don't give support for custom commands
- You should only implement a command from a developer that you trust, the command modules are given access to your entire bot, this includes your token, and some serious data.
- Only the modmail staff (users with the modmail role) are able to execute these commands

## Module
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

## Options
Functions that are available to command modules

| Key     | Description          |
| ------- | ------------------------------------------------------------------------------- |
| **bot** | The `client`, `utils` & `manager` objects (basically access to your entire bot) |
| **config** | Your config file |
| **message** | The message content |
| **args** | Arguments of the command |
