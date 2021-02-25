# Discord-ExpireBot

This Bot allows you to let roles expire. If you set e.g. the @voted role to 12h, the role will get removed automatically 12h after obtaining. This is individual to all users on the guild. It also saves the obtaining time into a JSON File, so if the Bot gets temporary offline, it can handle this.
[Support Server](https://discord.com/invite/ptpyaEPapy)

## Commands
`%help`<br>
`%expire <role> <time>` and `%unexpire <role> <time>`<br>
`%addperm <role>` and `%delperm <role>`<br>

## Credit
I didn't code it all on myself, I only helped and send feedback/did testing etc. The original Creator wants to stay private, so we decided to make the bot my own.
I'll probably host the bot and make it public for top.gg so anyone can use it, and I'll add multi-guild functuallity.<br>

Thanks to [DerSeb90](https://github.com/DerSeb90) for fixing a Critical Bug!!!

<details>
 <summary>I also want to say thank you to:</summary>
 <li> the guys from Scicraft's <a href="https://discord.com/channels/211786369951989762/423506375780466688">#coding-stuff</a> channel
 <li> the guys from <a href="https://discord.com/channels/724417775795306530">"The Garage"</a> (Armster15, F34R and Yumns) for the good advices.
</details>

## Invite
(currently only works on one server so its disabled)
https://discord.com/api/oauth2/authorize?client_id=786697105838309426&permissions=268438656&scope=bot

## Contributing
Consider giving this Repo a star if you like it and vote for the Bot at top.gg!!!<br>
Write issues and pulls! Test and Report! This helps the project.<br>
Also I don't mind donations ;)<br>
If you have any question or feedback, feel free to Contact me

## Selfhost or VPS
(I'd recommend to use a Raspberry Pi because it have to run 24/7 and bc its easier to setup)
You can also use a VPS
<details>
 <summary><b>Step-by-Step Tutorial</b></summary>
 
 ### Prerequisites
 You must have an account for Discord [[Link](https://discordapp.com/developers/applications/)]
  
 ### Creating a bot to get a bot token
 * Create an application in the developer portal by clicking [here](https://discordapp.com/developers/applications/)
 * Open up your new application and click 'Add Bot' under the Bot settings to create your bot.![Botscreen](https://user-images.githubusercontent.com/55095883/109214314-fba8ea00-77b1-11eb-8400-b34bf79c55ce.png)
 * Enable Both Intents ![intents_screen](https://user-images.githubusercontent.com/55095883/109213772-4bd37c80-77b1-11eb-9d63-9c8700cfd07c.png)
 * After creating the bot, click the 'Copy' button under the title Token. Take note of your token as you will need it later. Keep the token secret!!!!<br>![copytoken](https://user-images.githubusercontent.com/55095883/109214153-c3a1a700-77b1-11eb-909c-c9d5cf72701b.png)

<details>
 <summary><b>For Linux (Raspberry Pi)</b></summary>
  
 ### Downloading Repo and installing dependencies
 * Download the Repo as zip file and unpack it
 * Run `python3 -m pip install -r requirements.txt` in a Terminal to install dependencies
 
 ### Running the bot
 * Change the values in start.sh
  * discord_token=`(Enter the bot token that you copied from the developer portal)`
  * guild_id=`(Enter the ID of your Server. Rightclick on your Server on Discord and then click on 'Copy ID')`
 * Then doubleclick start.sh and click on "Open in Terminal" or run ./start.sh in a Terminal
 </details>
 <details>
 <summary><b>For Windows 10</b></summary>
 
 ### Downloading Repo and installing dependencies
 * Download the Repo as zip file and unpack it
 * Install [Python](https://www.python.org/downloads/) if you don't have it
 * open cmd (as admin) and cd to the repo
 * Run `pip install -r requirements.txt` to install dependencies
 
 ### Running the bot
 * Change the values in start.bat
   * set discord_token=`(Enter the bot token that you copied from the developer portal)`
   * set guild_id=`(Enter the ID of your Server. Rightclick on your Server on Discord and then click on 'Copy ID')`
 * Then doubleclick start.bat
 </details>
 
 <details>
 <summary><b>None of the above</b></summary>
 
 ### Downloading Repo and installing dependencies
  * Download the Repo as zip file and unpack it
  * install the missing requirements by running `pip install -r requirements.txt`
  
 ### Running the bot
  * find `os.environ.get('guild_id')` in the code (main.py) and replace it with your guild ID
  * find `os.environ.get('discord_token')` in the code (main.py) and replace it with you bot's token
  * Run main.py with python3
 </details>
</details>

## Host using Heroku (not recommended)
Check out the original tutorial from https://github.com/audieni/discord-py-heroku/
Note that Heroku doesn't have a persistent storage so you'd have to use some other storage addons.
<details>
  <summary><b>Step-by-Step Tutorial</b></summary>
  
 ### Prerequisites
 You must have an account for Discord [[Link](https://discordapp.com/developers/applications/)], GitHub [[Link](https://github.com/join)] , and Heroku [[Link (https://signup.heroku.com/)].

  ### Creating a bot to get a bot token
 * Create an application in the developer portal by clicking [here](https://discordapp.com/developers/applications/)
 * Open up your new application and click 'Add Bot' under the Bot settings to create your bot.![Botscreen](https://user-images.githubusercontent.com/55095883/109214314-fba8ea00-77b1-11eb-8400-b34bf79c55ce.png)
 * Enable Both Intents ![intents_screen](https://user-images.githubusercontent.com/55095883/109213772-4bd37c80-77b1-11eb-9d63-9c8700cfd07c.png)
 * After creating the bot, click the 'Copy' button under the title Token. Take note of your token as you will need it later. Keep the token secret!!!!<br>![copytoken](https://user-images.githubusercontent.com/55095883/109214153-c3a1a700-77b1-11eb-909c-c9d5cf72701b.png)

 ### How to fork the repository and set it up to work with Heroku?
 * Fork a copy of this repository by clicking the 'Fork' on the upper right-hand.
 * Create an application for Heroku by clicking [here](https://dashboard.heroku.com/new-app).
 * Under 'Settings', click on 'Reveal Config Vars' and enter the following:
   * KEY => discord_token
   * VALUE => (Enter the bot token that you copied from the developer portal)
   * Click the 'Add' button after entering all of this information.
 same for the GuildID:
   * KEY => guild_id
   * VALUE => (Enter the ID of your Server. Rightclick on your Server on Discord and then click on `Copy ID`)
   * Again, click the 'Add' button after entering all of this information.
 ![config vars](https://user-images.githubusercontent.com/55095883/103836278-e99bac80-5088-11eb-8283-b3744b3f587d.png)
 * Under 'Deploy', do the following:
   * Deployment Method => Connect your GitHub
   * App connected to GitHub => Search for the forked repository
   * Automatic Deploy => Enable Automatic Deploy (to redeploy after every commit)
   * It should look like something like this:
    ![deploy](https://user-images.githubusercontent.com/55095883/104065542-35bd2d00-5200-11eb-98e3-978ceb2af120.png)
 * Under 'Resources', do the following:
 ![worker](https://user-images.githubusercontent.com/13210233/103232638-fb52b680-4908-11eb-861d-767e59522b93.png)
   * Click on the 'Pencil' icon.
   * Switch the worker from off to on.
   * Click 'Confirm' to finalize the decision.
   * NOTE: You are allocated 550 free Dyno hours, which will not last the entire month. However, if you provide a credit card to verify your identity, you are given an additional 450 hours, which will allow your bot to run indefinitely.
  </details>
