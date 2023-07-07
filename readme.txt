Discord Bot Functionality -->

1. `import discord`: This line imports the `discord` module, which provides the functionality for interacting with the Discord API.

2. `import os`: This line imports the `os` module, which allows you to access operating system functionality. In this code, it's not being used explicitly, but it's a common practice to import `os` when working with environment variables or file paths.

3. `import random`: This line imports the `random` module, which provides functions for generating random numbers.

4. `token = "Your Token Here"`: This line defines a variable `token` and assigns it the value "Your Token Here". You should replace this placeholder value with the actual token of your Discord bot.

5. `bot = discord.Client()`: This line creates an instance of the `Client` class from the `discord` module. The `Client` class represents the connection to Discord and provides methods and events for interacting with the bot.

6. `@bot.event`: This is a decorator that indicates that the following function is an event handler.

7. `async def on_ready():`: This is an event handler function that is called when the bot has successfully connected to Discord and is ready to start receiving events. In this code, it simply prints "Bot is ready" to the console.

8. `@bot.event`: Another event handler decorator.

9. `async def on_message(message):`: This is an event handler function that is called whenever a message is sent in any channel that the bot can see. It takes the `message` object as a parameter, which represents the message that was sent.

10. `if message.author == bot.user: return`: This line checks if the author of the message is the bot itself. If it is, the function returns immediately to avoid any potential infinite loops where the bot responds to its own messages.

11. `if message.content.startswith("!hello"): await message.channel.send("Hello!")`: This line checks if the content of the message starts with "!hello". If it does, the bot sends a message "Hello!" to the channel where the message was received.

12. `if message.content.startswith("!random"): await message.channel.send(str(random.randint(1, 100)))`: This line checks if the content of the message starts with "!random". If it does, the bot generates a random number between 1 and 100 (inclusive) using `random.randint()` and sends it as a string to the channel where the message was received.

13. `bot.run(token)`: This line starts the bot and establishes a connection to Discord using the provided token. It is a blocking call, so any code placed after this line will not be executed until the bot is stopped or disconnected.

Overall, the code sets up a simple Discord bot that responds with "Hello!".

