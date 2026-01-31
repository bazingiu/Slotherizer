# Slotherizer

**Slotherizer** ensures you don't miss any updates in busy Discord text channels, thanks to automatic summaries generated with GPT-3.

## Getting Started
1. You will need a Discord bot to connect to the system. Create a new one by following this [guide](https://www.ionos.it/digitalguide/server/know-how/creare-un-bot-su-discord/)
   
   You will need the bot ***Token*** to add to the System configuration (Check this [guide](https://www.writebots.com/discord-bot-token/))
2. You will also need an [OpenAI](https://openai.com/api/) account to use the GPT-3 based APIs
   
   You will need:
   - The ***Organization ID*** (Which you can find on this [page](https://beta.openai.com/account/org-settings))
   - The ***API Key*** (Which you can find on this [page](https://beta.openai.com/account/api-keys))
3. Create the environment variable configuration file `.env` in the project root
   ```
   DISCORD_TOKEN="<Token>"
   ORGANIZATION="<Organization ID>"
   OPENAI_API_KEY="<API Key>"
   ```
4. Run `docker-compose up` to build and start **Slotherizer**

## How to use it
To use the **Discord bot** you must first *invite* it to your **Discord server** (Follow this [guide](https://www.writebots.com/discord-bot-token/#5_add_your_bot_to_a_discord_server)).

When the bot is in a server, you can invoke it in text chats using the command `!slotherizer <n>`, replacing `<n>` with the number of messages you want to summarize.

## Metrics
In this project, we use Kibana to visualize system usage metrics. There is a default version included that can be imported into Kibana as soon as it starts, providing a dashboard with some useful metrics: `kibana/monitoring.ndjson`
