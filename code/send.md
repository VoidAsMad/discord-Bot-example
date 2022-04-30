# Send Command

## bot command
### send
```py
@bot.command()
async def hello(ctx):
  await ctx.send('hello')
  
@bot.command()
async def ping(ctx):
  await ctx.send(f'{ctx.author.mention} pong!')
  ```
  
### reply
```py
bot command()
async def hello(ctx):
  await ctx.reply('hello!')
```

### embed
```py
@bot.command()
async def embed(ctx):
  embed = discord.Embed(title=f"Embed", description = "Send embed", color = 0xFF0000)
  ```

## Slash Command
### send
```py
@slash.slash(name="hello",description="print hello",guild_ids=[guild_id])
async def hello(ctx):
  await ctx.send('hello')
  
@slash.slash(name="hello",description="print pong",guild_ids=[guild_id])
async def ping(ctx):
  await ctx.send(f'{ctx.author.mention} pong!')
  
#hidden
@slash.slash(name="hello",description="print hello",guild_ids=[guild_id])
async def hello(ctx):
  await ctx.send('hello', hidden = Ture)
  
@slash.slash(name="pong",description="print pong",guild_ids=[guild_id])
async def ping(ctx):
  await ctx.send(f'{ctx.author.mention} pong!', hidden = Ture)
  ```
  
### reply
```py
@bot.command()
async def hello(ctx):
  await ctx.reply('hello!')
```

### embed
```py
@bot.command()
async def embed(ctx):
  embed = discord.Embed(title=f"Embed", description = "Send embed", color = 0xFF0000)
  ```
