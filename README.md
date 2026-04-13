from email.mime import message

import discord
import os
intents = discord.Intents.default()
intents.message_content = True
client = discord.Client(intents=intents)
@client.event
async def on_message(message):
if message.author == client.user:
return
if message.content.startswith('poniedziałek'):
await message.channel.send("informatyka")
elif message.content.startswith('wtorek'):
await message.channel.send("piłka nożna")
elif message.content.startswith('środa'):
await message.channel.send("basen")
elif message.content.startswith('czwartek'):
await message.channel.send("piłka nożna")
elif message.content.startswith('piątek'):
await message.channel.send("wolne")
elif message.content.startswith('sobota'):
await message.channel.send("wolne")
elif message.content.startswith('niedziela'):
await message.channel.send("wolne", "wieczorem meczarnia")
