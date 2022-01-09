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
Note: You can add the bot into two servers if you want to have a private server just for the modmail threads.
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
  3. Use the invite link below to invite the bot to your server(s)

## 4. Create a Database
A database is required for this modmail bot. The bot will be storing datas such as modmail logs and bot configurations such as blocked users, snippets, and .etc. This modmail bot only supports [MongoDB Atlas](https://www.mongodb.com).
  1. Visit https://www.mongodb.com
  2. Create an account if you haven't already
  3. Create a database > Create a database user > Whitelist all IP's
  4. Obtain a database connection URI (e.g. `mongodb+srv://Username:<password>@modmail.mongodb.net/`)
  5. Copy the connection URI and paste it on somewhere private (e.g local notepad)
  6. Replace the `<password>` with the password for the user.

# Setting Up

## 5. Clone this repository
Open your terminal/command prompt and type/paste in the command below:
```
git clone https://github.com/BotStudios/modmailbot.git
```

## 6. Edit the configuration file
After using the clone command, you should see a folder named `modmailbot` inside the folder you create. Now, head over to [this](https://github.com/BotStudios/modmailbot/wiki/Configuration) page to learn more about bot configurations. You can head right back after configuring your bot.

## 7. Startup the bot
After going through those necessary steps, its time to try if the bot works. You can straight away open the `start.bat` file if you're on a Windows device. You should be able to startup the bot without opening `start.bat`, or if you're on a linux or macOS device:

  *The following assumes basic knowledge about using command line tools.*
  - Run `npm ci` in the modmail bot folder before first start up and after every update
  - Run `npm start` in the modmail bot to start the bot
  

  

  