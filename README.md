
# Workshop Discord bot - Beginner

This Workshop is an introduction of what you can do with DiscordJs


## SetUp

Init my project with npm

```bash
    npm init
```


Install Discordjs

```bash
    npm install discord.js
```

Go to your Discord app and activate the developer mode


Dev portal:

Go to the discord dev portal : https://discord.com/developers/applications

Add a new application and give it a name

Go to bot page

Add a bot

View Token and copy it somewhere

Then allow all privileged gateway intents


Got to the OAuth2 URL generator

in **Scope**  give the bot role and the applications.commands role 

Then in the **Bot Permissions** allow Admin

copy the **Generated URL** and paste it in your browser

Select a server

## Create files

* Store the token in a secure way

    * Create an .env file
    * Create a var TOKEN=<your token>

* Create a src/ directory

    * Create a file name : index.js (it will be the main of your project unless you change the entry point during the **npm init**)

* Make a .gitignore

    * .gitignore
    * node_modules/
    * .env

## Bot first functions

This link will help you to start your discord bot : https://discordjs.guide/creating-your-bot/main-file.html

You can use **import** or **require**, use the one you like the most (man google)

Unlike the link above we're gonna use dotenv to retrive our **token**

```bash
    npm install dotenv
```

Your client should look like this :
```js
    const client = new Client({
        intents: [
            GatewayIntentBits.Guilds,
            GatewayIntentBits.GuildMessages,
            GatewayIntentBits.MessageContent,
            GatewayIntentBits.GuildMembers,
            GatewayIntentBits.GuildIntegrations,
        ],
    });
```

It enable all we need to have to code the exercices


## Start

```bash
    cd src/
    node .
```

If everything work fine well done we can head to the exercices

## Exercice 1 - Greetings

Make a function that say hello with a ping to the user in the "général" channel when a new user is add in the server

Then send an embed in the "bienvenue" channel with a message containing the name of the user and the number of people in the server

*Bonus* : add the avatar of user

## Exercice 2 - Ping Command

You need to reply **pong** when a user send **ping**

This exercice can be made with 2 methods

* Easy - Check the content of the message and reply
* The good way - make a slash command that reply

The second method is not hard when your *read the doc* : https://discordjs.guide/creating-your-bot/slash-commands.html

then

https://discordjs.guide/creating-your-bot/command-deployment.html

## Exercice 3 - Assignment of roles

You have to make slash command that send a discord message containing several buttons to choose roles

*read the doc* : https://discordjs.guide/interactions/buttons.html#buttons

You can hard code the number of buttons or make it adaptative (json, xms, yaml, etc ..)

*Bonus* : when a user click a role he already have the bot remove it


## Bonus

* Error handling you wouldn't have thought of
* Anything you want (try to impress your Astek)
