# Configure

## 1. Open the config file
Open the `config.js` file in the bot's folder. If you don't have a code editor software such as Visual Studio Code, you can simply open the file with a text editor.

## 2. Configuration Variables
View an example of [configured config.js]()

| Key       | Description                                                        |
| --------- | ------------------------------------------------------------------ |
| `token`     | Your Bot's Token (e.g. `MjQ1NTU5MDg3NGI0MjE2ODMy.AulyxA.brcD2xRAqjACTuMcGPwy4TWVQdg`) |
| `databaseURI` | Your MongoDB Database URI (e.g. `mongodb+srv://Username:<password>@modmail.mongodb.net/`) |
| `guildID` | Your modmail thread server ID (the server you use to receive modmails) |
| `category` | ID of the category where threads will be created |
| `roleID` | ID of the role for modmail staff(s) (users without this role cannot reply, view, delete modmails) |
