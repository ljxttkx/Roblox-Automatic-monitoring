const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({
  intents: [
    GatewayIntentBits.Guilds,
    GatewayIntentBits.GuildMessages,
    GatewayIntentBits.MessageContent,
  ],
});

client.on('ready', () => {
  console.log(`Bot online as ${client.user.tag}`);
});

client.on('messageCreate', (message) => {
  if (message.content === 'ping') {
    message.reply('Pong from Railway!');
  }
});

// 从 Railway 环境变量读取 Token
client.login(process.env.DISCORD_TOKEN);
