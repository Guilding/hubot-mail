# hubot-mail

[![Build Status](https://travis-ci.org/ClaudeBot/hubot-mail.svg)](https://travis-ci.org/ClaudeBot/hubot-mail)
[![Dependency Status](https://david-dm.org/ClaudeBot/hubot-mail.svg)](https://david-dm.org/ClaudeBot/hubot-mail)

A Hubot script for preparing messages that will be delivered upon the recipient's next activity (i.e. joins room, enters a message).

See [`src/mail.coffee`](src/mail.coffee) for full documentation.


## Installation via NPM

1. Install the __hubot-mail__ module as a Hubot dependency by running:

    ```
    npm install --save hubot-mail
    ```

2. Enable the module by adding the __hubot-mail__ entry to your `external-scripts.json` file:

    ```json
    [
        "hubot-mail"
    ]
    ```

3. Run your bot and see below for available config / commands


## Configuration

Variable | Default | Description
--- | --- | ---
`HUBOT_MAIL_KEY` | _mail | The unique key used for persistence (storing/retrieving mails from memory)


## Commands

Command | Listener ID | Description
--- | --- | ---
hubot mail `recipient` `message` | `mail.new` | Sends a `message` to `recipient` when found available
hubot unmail `[recipient]` | `mail.cancel` | Deletes all mail sent by you. Optionally, if `recipient` is specified, only mail sent to `recipient` by you will be deleted


## Sample Interaction

```
user1>> hubot mail user1 Hello world!
hubot>> user1: Are you sure you want to send a mail to yourself? Sad.
```
