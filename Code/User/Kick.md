# Kick Command

## No slash command
```py
@bot.command(aliases=['킥','kick'], pass_context=True)
async def _kick(ctx, *, user_name: discord.Member, reason='없음')
  await user.kick(reason=reason)
  embed = discord.Embed(
      title="유저추방(User Kick)", 
      description=f"<@{user.id}>님을 추방하였습니다.", 
      color=0x4374D9
    )
  embed.add_field(
      name="사유(Reason)", 
      value=reason, 
      inline=False
    )
  await ctx.reply(embed=embed)
```


## Slash command
```py
@slash.slash(name="kick",description="유저를 추방합니다.(재입장가능)")
async def kicks(ctx, user : discord.Member, reason = None):
  await user.kick(reason=reason)
  embed = discord.Embed(
      title="유저추방(User Kick)", 
      description=f"<@{user.id}>님을 추방하였습니다.", 
      color=0x4374D9
    )
  if reason == None:
    reason = '없음'
  embed.add_field(
      name="사유(Reason)", 
      value=reason, 
      inline=False
    )
  await ctx.reply(embed=embed)
```
