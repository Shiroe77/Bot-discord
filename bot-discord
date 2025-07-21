import os
from dotenv import load_dotenv
import random
import discord
from discord.ext import commands
from keep_alive import keep_alive

load_dotenv()
token = os.getenv('DISCORD_TOKEN')

intents = discord.Intents.default()
intents = discord.Intents.default()
intents.message_content = True
intents.members = True

bot = commands.Bot(command_prefix='!', intents=intents)


@bot.command()
async def bonjour(ctx):
    await ctx.send(f"Bonjour {ctx.author} !")


@bot.command()
async def ping(ctx):
    await ctx.send(f"Pong {ctx.author} !")


@bot.command()
async def pileouface(ctx):
    await ctx.send(random.choices(["Pille", "Face"]))


@bot.command()
async def roll(ctx):
    await ctx.send(random.randint(1, 100))


# Liste de blagues
blagues = [
    "Pourquoi les canards ont-ils autant de plumes ? Pour couvrir leur derrière !",
    "Que dit une maman tomate à son bébé tomate ? Dépêche-toi, ketchup !",
    "Pourquoi les plongeurs plongent-ils toujours en arrière et jamais en avant ? Parce que sinon ils tombent dans le bateau.",
    "Comment appelle-t-on un alligator en gilet ? Un investigateur.",
    "J’ai acheté un chien à trois pattes, je l’ai appelé 'Trépied'.",
    "Deux antennes se marient. La cérémonie était nulle, mais la réception était incroyable.",
    "C’est l’histoire d’un pingouin qui respire par les fesses… un jour il s’assoit et il meurt.",
]


@bot.command()
async def joke(ctx):
    blague = random.choice(blagues)
    await ctx.send(blague)


token = os.environ['TOKEN_BOT_DISCORD']

keep_alive()
bot.run(token)
