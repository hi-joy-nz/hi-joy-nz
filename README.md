## Table of contents
- [Contact & about me](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#contact--about-me)
- [Projects](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#projects)
  - [JoyBot (Python)](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#joybot-python)
  - [SafeBot (Python)](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#safebot-python)


## Contact & about me
- Find all the details on [my site](https://hi-joy-nz.github.io/)

## Projects
### JoyBot (Python)
- JoyBot was my first large Discord bot, containing:
  - Legacy text-based commands
  - A spawn and collection system
    - Users spawn and collect a variety of over 300 unique spawns <br>
    ![Detailed collection command](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/JoyBot%20Examples/Detailed%20spawn%20collection.png)
    - Users can race to find 'Challenge Spawns' - a randomly selected spawn that rewards users with 'Challenge Points' when found <br>
    ![Challenge spawns and points](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/JoyBot%20Examples/Challenge%20spawns%20and%20points.png)
  - A truth or dare game
  - A fun fact command
  - A fishing command
  - A "who is most likely to" question command
  - A channel slowmode adjustment command 
- JoyBot is hosted on my Raspberry Pi, and is currently used actively in a private server of nearly 50 members with frequent updates
- JoyBot is made with [discord.py](https://discordpy.readthedocs.io/en/stable/)

See [more examples](https://github.com/hi-joy-nz/hi-joy-nz/tree/main/Examples/JoyBot%20examples) of JoyBot being used

*[Return to table of contents](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#table-of-contents)*

### SafeBot (Python)

**[Read SafeBot's documentation](https://hi-joy-nz.github.io/SafeBot/Docs)**
- SafeBot is my first attempt to make a complete multipurpose Discord bot that uses [slash-commands](https://discord.com/blog/welcome-to-the-new-era-of-discord-apps?ref=badge), and is far more advanced than JoyBot, containing:
  - A complete slash command and embed system
  - Error handling for all commands with developer logs for unexpected errors
  - A currency system
    - Users can earn and spend a currency from a balance stored in an external file
    - (Work in progress) Store and purchasing system with real-time store updates, with all store information managed with an external JSON file <br>
  ![Balance command](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Points%20balance.png)
  - A complete ticketing system
    - Users can create a private channel with staff, and are able to add extra users into the ticket
  - Pokémon collecting game
    - Every 2 minutes, users can spawn a random Pokémon
      - Pokémon are spawned based on the area the user selected, and the rarity of the Pokémon
      - All Pokémon have a small chance to be [shiny](https://bulbapedia.bulbagarden.net/wiki/Shiny_Pok%C3%A9mon), which is influenced by their rarity; with rarer Pokémon having a higher chance to be shiny <br>
  ![Example encounter](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Pokemon%20spawn%20(city).png)
    - Users can view their collection <br>
    ![Collection](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Pokemon%20collection%20(page%201).png)
      - They can also apply certain filters <br>
      ![Collection with shiny filter](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Pokemon%20collection%20(shiny).png)
    - Users can view the Pokémon that spawn in a specified area, sorted by rarity <br>
    ![Spawns in volcano area](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Pokemon%20spawns%20(volcano).png)
    - Users can view details about a Pokémon they have caught <br>
    ![Info panel](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Pokemon%20info%20(1).png)
  - An about user command
    - Gets and displays data about a provided user from the Discord API <br>
    ![About command](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/About%20user.png)
  - A Spotify search command
    - Searches Spotify's API for a term and provides details about the top result <br>
    ![Spotify search command](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Spotify%20search.png)
  - A random colour generator <br>
  ![Random colour generator](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/Examples/SafeBot%20Examples/Random%20colour%20(1).png)
  - Moderation commands
    - Mute, unmute, and slowmode control commands
- Safebot's commands: Public
  - `/about <user>` : Provides details about a Discord user from Discord's API
  - `/balance [user]` : View your balance or another user's balance
  - `/buy <itemID>` : (Work in progress) Purchases an item from the store and adds it to your inventory
  - `/coinflip` : Flip a coin, it can land on heads or tails 
  - `/daily` : Collect free points once every 24 hours
  - `/help` : Provides a list of commands and their uses
  - `/pokemon_collection` : Displays a list of every Pokémon a user has caught, and displays them in pages (20 per page)
  - `/pokemon_info <number>` : Displays information about a Pokémon you have caught, where `number` is the Pokémon's Collection Number (number in your collection)
  - `/pokemon_spawn <area>` : Spawns a random Pokémon from `area`'s spawn pool
  - `/pokemon_spawns <area>` : Shows a list of all Pokémon that can be found in `area` and their rarity
  - `/random_colour` : Generates a random colour, and provides both hex and RGB values
  - `/spotify_search <search>` : Searches the SPotify API for `search` and provides information about the top result
  - `/store` : (Work in progress) Displays the current store, with the ID, name, and price of each item
  - `/ticket_add <user>` : Adds `user` to the current ticket if not already in it
  - `/ticket_close` : Asks the user for confirmation, then closes the current ticket
  - `/work` : Use this and wait 2 hours to claim extra free points
- SafeBot's commands: Server moderation
  - `/mute <user> <length> <reason>` : Mutes `user` for `length` minutes with the reason `reason`
  - `/set_slowmode <cooldown>` : Sets current channel's slowmode to `cooldown` seconds
  - `/staff_help` : Provides a list of moderation and management commands
  - `/starboard_info` : Provides details about the starboard feature
  - `/ticket_create_gui` : Sends the create ticket embed and button to the current channel
  - `/ticket_remove <user>` : Removes `user` from the current ticket
  - `/unmute <user> <reason>` : Unmutes `user` if muted, with reason `reason`
- SafeBot's commands: Bot management
  - `/change_points <user> <change>` : Changes `user`'s points balance by `change`
  - `/change_points_all <change>` : Changes all user's points balance by `change`
  - `/set_bot_status <status_type> <text>` : Changes the bot's presence to `status_type` `text`
- SafeBot is still being developed, and will be hosted on my Raspberry Pi for use in my public Discord server
- SafeBot is made with [discord.py](https://discordpy.readthedocs.io/en/stable/)

See [more examples](https://github.com/hi-joy-nz/hi-joy-nz/tree/main/Examples/SafeBot%20Examples) of SafeBot being used


*[Return to table of contents](https://github.com/hi-joy-nz/hi-joy-nz/blob/main/README.md#table-of-contents)*## Hi there 👋

<!--
**hi-joy-nz/hi-joy-nz** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
