# Frequently Asked Questions

## 1. Listeners/Event Handling
You can customize this bot with listeners, having custom replies and able to perform some really cool actions when something happens (e.g. When someone closes a thread or when someone opens a thread and many more). But be aware of anything you're doing inside the listener as it might crash or cause the bot to malfunction.
 - **Things To Be Aware Of:**
      - Deleting Messages
      - Sending Messages
      - Reacting To Messages
      - Editing Channels

## 2. What's the `customReply` option in the config file for ?
(for some serious situation that requires some actions to prevent confusion)

## 3. Support for other databases
This modmailbot only supports (currently) MongoDB, as its hard for us to add support for more databases. With that said, if you can, please do contribute codes that adds support for other databases. 🤗🤗

## 4. Why MongoDB
We chose MongoDB as its simple to setup and use with the help of [mongoosejs](https://npmjs.com/mongoose).