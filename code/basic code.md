# No slash Command
```py
import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='?', intents=discord.Intents.all())

@bot.event
async def on_ready():
  print('로딩완료')
  
@bot.command()
async def ping(ctx):
  await ctx.send('pong!')
  
bot.run(token)
```

# Slash Command
```py
import discord
from discord.ext import commands
from discord_slash import SlashCommand, SlashContext

bot = commands.Bot(command_prefix=['?'], intents=discord.Intents.all())
slash = SlashCommand(bot, sync_commands=True)

@bot.event
async def on_ready():
  print('로딩완료')
  
@slash.slash(name="ping",description="pong을 대답합니다.",guild_ids=[your guild id])
async def ping(ctx):
  await ctx.send('pong!')

bot.run(token)
```
