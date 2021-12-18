# Get Started
**Don't hesitate to join our [support server](https://discord.com/invite/2JcXU8uJKY) if you need any help related to this bot.**

## 1. Install [node.js](https://nodejs.org) on your machine
Install [node.js](https://nodejs.org) if you haven't already. You'll need this in order to run the modmail bot.

## 2. Create a [Discord Bot](https://discord.com/developers/applications)
  1. Visit the [Discord Developer Portal](https://discord.com/developers/applications) 
  2. Click New Application 
  3. Goto Bot
  4. Click Add Bot
  5. Uncheck "Public Bot"
  5. Enable "Presence Intent", "Server Members Intent" & "Message Content Intent"
  6. Copy the token and paste it on somewhere private (e.g. local notepad)

## 3. Invite the Discord Bot to a server
  1. Goto OAuth2 > URL Generator 
  2. Select **bot** then scroll down and select these permissions (view [image example](https://user-images.githubusercontent.com/91641514/146574207-50080821-2303-40ab-bdff-d5ef98ff40e5.png)):
     - View Audit Log
     - Manage Channels
     - Manage Webhooks
     - Read Messages/View Channels
     - Send Messages
     - Manage Messages
     - Embed Links
     - Attach Files
     - Read Message History
     - Use External Emojis
     - Add Reactions
  3. Use the invite link below to invite the bot to your server

## 4. Create a Database
A database is required for this modmail bot. The bot will be storing datas such as modmail logs and bot configurations such as blocked users, snippets, and .etc. This modmail bot currently supports [MongoDB Atlas](https://www.mongodb.com) only.
  1. Visit https://www.mongodb.com
  2. Create an account if you haven't already
  3. Create a database > Create a database user > Whitelist all IP's
  4. Obtain a database connection URI (e.g. `mongodb+srv://Username:<password>@modmail.mongodb.net/`)
  5. Copy the connection URI and paste it on somewhere private (e.g local notepad)
  6. Replace the `<password>` with the password for the user.

# Setting Up
Its time to move on !

## 5. Cloning this repository
    1. Go ahead and open your terminal or command prompt then type `cd`
    2. Create a folder for this project somewhere on your computer and drag the folder onto the terminal/command prompt and hit enter
    3. type/paste in the command below:

    ```
    git clone https://github.com/BotStudios/modmailbot.git
    ```

## 6. Edit the configuration file
After using the clone command, you should see a folder named `modmailbot` inside the folder you create. Now, its time to configure the bot.
   1. Open the `modmailbot` folder if you haven't already
   2. Then open the `config.js` file (if you don't have a code editor such as visual studio code, you'll have to right click and open the file with a built in text editor)
   3. You should something like this:

   ```
module.exports = {
    databaseURI: '',
    port: 3000,
    token: '',
    guildID: '',
    category: '',
    roleID: '',
    activity: '',
    prefix: '',  
    logThreads: true,
    notifyMsg: '',
    webhookURI: '',
    logsURI: '',
    colors: { 
        success: '',
        error: '',
        primary: '',
        custom: ''
    }
}
```
*it doesn't matter if its the same or not as long as you can see the `token` and the `databaseURI` property.
  

  