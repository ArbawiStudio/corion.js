![](https://media.discordapp.net/attachments/863696103525187604/1026960225925873774/corion.js_1.png)

## Install Package

<br>

```js
$ npm i corion.js
```

## Setup Package

<br>

```js
const { Client } = require('discord.js')
const client = new Client({ intents: ['Guilds', 'GuildMessages', 'GuildMembers'] })
const { DiscordLogger } = require('corion.js')
DiscordLogger.setup(client) // For Discord Logger Only!
```

## Discord Logger

<br>

```js
client.on('MemberJoined', async(Member) => {
    if(Error) return console.error(Error)
    const Channel = Member.guild.channels.cache.get('')
    if(!Channel) return;
    Channel.send({ content: `${Member} has been Joined; 
    Joined Discord : <t:${parseInt(Member.createdAt / 1000)}:f>` })
})

client.on('MemberBoostAdd', async Member => {
    const Channel = Member.guild.channels.cache.get('')
    if(!Channel) return;
    Channel.send({ content: `${Member} has been boosted the server!` })
})

client.on('MemberBannedAdd', async (Member, User) => {
    const Channel = Member.guild.channels.cache.get('')
    if(!Channel) return;
    Channel.send({ content: `${Member} has been banned; by ${User}` })
})

client.on('MemberBannedRemove', async (Member, User) => {
    const Channel = Member.guild.channels.cache.get('')
    if(!Channel) return;
    Channel.send({ content: `${User} has been deleted banned; from ${Member}` })
})
```

## ButtonPaginator

<br>

```js
const { ButtonPaginator } = require('corion.js')
client.on('messageCreate', async TOBZi => {
    if(TOBZi.content.startsWith(Prefix + 'help')) {
        const Page1 = new EmbedBuilder() .setDescription('Page 1')
        const Page2 = new EmbedBuilder() .setDescription('Page 2')
        const Page3 = new EmbedBuilder() .setDescription('Page 3')
        const Page4 = new EmbedBuilder() .setDescription('Page 4')
        const Page5 = new EmbedBuilder() .setDescription('Page 5')
        const Back  = new Discord.ButtonBuilder() .setStyle(ButtonStyle.Danger)  .setEmoji('◀')
        const Next  = new Discord.ButtonBuilder() .setStyle(ButtonStyle.Success) .setEmoji('▶')
        await ButtonPaginator(TOBZi, [Page1, Page2, Page3, Page4, Page5], [Back, Next])
    }
})
```
<br>

# Features

- **`Discord Logger`**
- **`ButtonPaginator`**
- **`ProBotTax Calculate (Coming 6/10/2022)`**
- **`Invite Tracker (ComingSoon 6/10/2022)`**

<br>

# Developers of the Package

- **`TOBZi`** 
  -

<br> 

---

<br>
<a href='https://discord.gg/9mxaKNR9fN' target="_blank"><img alt='Discord' src='https://img.shields.io/badge/TOBZi-100000?style=flat-square&logo=Discord&logoColor=FFFFFF&labelColor=5F54FF&color=5F54FF'/></a> <a href='https://instagram.com/moearabie' target="_blank"><img alt='Instagram' src='https://img.shields.io/badge/Instagram-100000?style=flat-square&logo=Instagram&logoColor=FFFFFF&labelColor=F77737&color=F77737'/></a>
