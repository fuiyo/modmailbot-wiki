# Configure

## 1. Open the config file
Open the `config.js` file in the bot's folder. If you don't have a code editor software such as Visual Studio Code, you can simply open the file with a text editor.

## 2. Configuration Variables
View an example of [configured config.js](https://user-images.githubusercontent.com/91641514/146630100-154e1af8-c064-4541-9b92-c7bf184225db.png)

| Key       | Description                                                        | Required |
| --------- | ------------------------------------------------------------------ | -------- |
| `token`     | Your Bot's Token (e.g. `MjQ1NTU5MDg3NGI0MjE2ODMy.AulyxA.brcD2xRAqjACTuMcGPwy4TWVQdg`) | true |
| `databaseURI` | Your MongoDB Database URI (e.g. `mongodb+srv://Username:<password>@modmail.mongodb.net/`) | true |
| `guildID` | Your modmail thread server ID (the server you use to receive modmails) | true |
| `category` | ID of the category where threads will be created | true |
| `roleID` | ID of the role for modmail staff(s) (users without this role cannot reply, view, delete modmails) | true |
| `prefix` | The prefix of the bot | true |
| `colors` | Specify the colors for `primary`, `success`, `error` and `custom` | true |
| `customReply` | Able to customize replies in some situation | false |
| `activity` | Your Bot's Status | false |
| `threadCloseDelay` | Delay (deleting a channel) after a staff runs the close or delete thread command | false |
| `logThreads` | Threads logging (log the thread when someone closes a thread) | false |
| `notifyMsg` | A notification message when someone creates a thread (such as pings and .etc) | false |
| `webhookURI` | Webhook that will be trigger when someone closes a thread | false |
| `logsURI` | Threads logging URL | false |
| `port` | The port where modmail logs viewer will be hosted (this will enable the logs viewer) | false |



