<div dir="auto">

<p align="center">
  <img src="https://cdn.discordapp.com/attachments/826890223916154903/875037160280051752/unknown.png" />
  
</p>
<div align="center">

# یک داکیومنت برای شما🐱‍👤
</div>

# 📃پیش نیاز ها

* [Node.js v16+](https://nodejs.org/en/download/releases/)
* [Discord.js](https://www.npmjs.com/package/discord.js)
* [dotenv](https://www.npmjs.com/package/dotenv)
* [mongoose](https://www.npmjs.com/package/mongoose)
* و فراموش نکنید که حتما باید یک اپلیکیشن و ربات در دولوپر پورتال دیسکورد بسازید
* https://discord.com/developers/applications
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875073281605111918/unknown.png" />

* تیک اپلیکیشن کامند رو هم حتما موقع اینوایت بات به سروتون رو از توی دولوپر پورتال حتما بزنید چون نیازش دارید
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875301636355018822/unknown.png" />

* دولوپر مود دیسکوردتون رو هم روشن کنید که بتونید ایدی هایی که نیاز دارید رو کپی کنید
  <img src="https://cdn.discordapp.com/attachments/826890223916154903/875052912227786822/dev-m.gif" width="510" height="290"/>


# 🕚قبل از شروع
 
این ریپو برای این ساخته شده که به شما کمک بکنه که بتونید از صفر بدون نگرانی و استرس کار های باحالی رو انجام بدید که شاید به نظرتون در نگاه اول سخت بیاد
  پس صاف بشینید و خوب مثال هارو **ببینید** **یاد بگیرید** و ازشون کلی ایده های خفن بگیرید و ببرید توی ادیتور هاتون که بتونید چیزای قشنگ خلق بکنید🎇

# 😃خب بیا شروع کنیم

- ما الان میخایم از یه پکیج به نام ``discord.js`` استفاده بکنیم که لینکش توی لیست پیش نیاز های بالا هست
- توجه داشته باشید که حتما ``node.js`` رو نصب کرده باشید و ورژن اون بالای 16 باشه
- در این اموزش زیاد با واژه ای ``guild`` رو به روی میشید که در واقع همون معنای سرور رو میده ``server``

استاندارد ترین روش برای ساخت یک کامند در دیسکورد جی اس با اسلش کامند هستش که اول باید یه کامند رو برای بات ریجستر بکنیم
<br>
<br>
<br>
**2 نوع اسلش کامند وجود داره**


* guild command / کامند برای یک سرور


* global command / کامند برای بات که به صورت کلی هست

ما با نوع اول شروع میکنیم که هم سریع تره هم برای توسعه بهتره
<br>
برای ساخت کافیه توی یه پوشه یک فایل بسازید به نام ``register-command.js``
<br>
بعد از اون کافیه که کد مثال زیر رو توی اون وارد بکنید
<br>
<div dir="ltr">


```javascript
const { REST } = require('@discordjs/rest');
const { Routes } = require('discord-api-types/v9');

let token = 'TOKEN';
let guild_ID = 'SERVER_ID';
let client_ID = 'BOT_ID';

const commands = [{
  name: 'ping',
  description: 'in cmd mamolan dar javab mige [pong!] :)'
}]; 

const rest = new REST({ version: '9' }).setToken(token);

(async () => {
  try {
    console.log('dar hal ezafe kardn (/)command be server');

    await rest.put(
      Routes.applicationGuildCommands(client_ID, guild_ID),
      { body: commands },
    );

    console.log('(/) command shoma be server mored nazar ezafe shod');
  } catch (error) {
    console.error(error);
  }
})();
```


</div>
<br>
  خب هدف ما الان اینه که جای چنتا چیزو با چیزایی که میخایم عوض بکنیم
  
<div dir="ltr">

```javascript
let token = 'TOKEN';
let guild_ID = 'SERVER_ID';
let client_ID = 'BOT_ID';
```

</div>
  
**توی کد بالا 3 تا متغیر وجود داره**
<br>
  1-``token``
  
  2-``server_ID``
  
  3-``client_ID``
  
  <br>
  
  
- token:
  - میتونید این متغیر رو از دولوپر داشبورد و قسمت بات در اپلیکیشن و باتی که ساختید بگیرید
    <img src="https://cdn.discordapp.com/attachments/826890223916154903/875121251407003679/bot-token.png" />

- server id:
  - برای گرفتن ایدی سرور نیازه که دولوپر مود دیسکوردتون رو روشن کنید که توی پیش نیاز ها توضیح داده شده
      - فقط کافیه روی ایکون سرور راست کلیک بکنید و بعدش کپی ایدی رو بزنید تا ایدی سرور کپی بشه
    <img src="https://cdn.discordapp.com/attachments/826890223916154903/875131765486927942/unknown.png" />
  
  
- client id:
  - برای کپی کردن ایدی ربات هم کافیه مثل سرور روی بات کلیک کنید و گزینه کپی ایدی رو بزنید
    
    <img src="https://cdn.discordapp.com/attachments/826890223916154903/875132737072291840/unknown.png" />

**بعد از این که متغیر هارو درست عوض بکنید دارید به یه همچین چیزی توی اون قسمت نگاه میکنید**

<div dir="ltr">
  
    
```javascript
let token = 'ODy3Msdak4MjNzEyNjDU0.nmhg.xcE4Nj77nbEY5Rk4YU_6YwR_Tio';
let guild_ID = '763773594547126272';
let client_ID = '837098281712615454';
```

</div>

بعدش که جای متغیر هارو عوض کردید فقط کافیه که فایل رو ذخیره بکنید و بعدش با ``node.js`` اونو ران بکنید
<br>
  - ``node register-command.js``
  
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875297595189256223/unknown.png" />

خب همون جوری که دیدید ما اسلش کامندمون رو به راحتی درست کردیم
<br>
و وقتی الان بریم توی سرور موردنظر و تایپ بکنیم ``ping/`` میبینیم که برای بات یک دستور پینگ با توضیحاتی که نوشته بودیم ساخته شده
<br>
<br>
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875302762630496266/unknown.png" />
<br>
<br>
برای اضافه کردن اسلش کامند برای همه ای سرور های بات هم فقط کافیه که یک قسمت از کد اولیه بالا رو عوض بکنید که 2 تا نکته وجود داره❕
  - اضافه شدن هر دستور به صورت گلوبال در ربات چیزی حدود 1 ساعت زمان میبره از طرف API دیسکورد
  - ما این نوع اضافه کردن رو برای کار های تستی پیشنهاد نمیکنیم و بهتره اول دستورات خودتون رو توی یه سرور تست اضافه و تست کنید و بعدش اونا رو به صورت گلوبال منتشر کنید
<br>

<div dir="ltr">

```javascript
await rest.put(
	Routes.applicationCommands(CLIENT_ID),
	{ body: commands },
);
```

</div>

<br>

**خب بعد از اینکه ما دستور رو به سرور اضافه کردیم فقط کافیه که اونو فعال بکنیم اسونه نه؟**
<br>
با ساخت یه فایل به نام ``bot.js`` شروع میکنیم
<br>
و بعدش میایم کد مثال زیر رو توی اون قرار میدیم
<br>

<div dir="ltr">

```javascript
const { Client, Intents } = require('discord.js');
const client = new Client({ intents: [Intents.FLAGS.GUILDS] });
let token = 'TOKEN';

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('interactionCreate', async interaction => {
	if (!interaction.isCommand()) return;

	if (interaction.commandName === 'ping') {
		await interaction.reply('Pong!');
	}
});

client.login(token);
```

</div>
<br>
الان توی کد بالا تنها چیزی که نیازه که عوض بشه متغیر توکن هستش که خب مثل کد اول فقط نیازه از دولوپر پورتال کپی و پیست کنیدش 
<br>
بعد از گذاشتن توکن فقط کافیه که فایل رو ذخیره و ران بکنید
<br>

- ``node bot.js``
<br>
<br>

<img src="https://cdn.discordapp.com/attachments/826890223916154903/875314328146960464/unknown.png" />
<br>

اگه با همچین پیامی رو به رو شدید یعنی ربات شما اماده به کار هستش
<br>

و الان دیگه فقط کافیه برید توی سروری که کامند رو توش ثبت کردید و تایپ بکنید ``ping/`` و اینتر رو فشار بدید
<br>

- 🎉 هورا! همون طوری که میبینید بات در جواب دستور شما گفت ``!Pong`` 
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875314924006572092/unknown.png" />
<br>
<br>


# 🚀یه پروژه همیشه کوچیک نمیمونه! 

**ما توی اموزش بالا به شما پایه ترین راه برای درست کردن یه دستور و راه اندازی اون رو اموزش دادیم ولی یه سری چیز ها رو باید برای نظم عوض بکنید**
<br>
	
دیدید که برای استفاده از توکن سرور ایدی یا ایدی بات اونا رو توی خود کد تعریف میکردیم
<br>
	
ولی این کار در یه پروژه ای استاندارد توصیه نمیشه و بهتره شما یه کانفیگ فایل داشته باشید که اطلاعات مهمی که نیاز دارید توی اون تعریف بشه و بعد بتونید به راحتی اونارو تو کد خودتون استفاده بکنید
<br>

برای استفاد از یه کانفیگ ها توی یه کد روش های زیادی هست ولی ما میخایم اینجا از پکیج ``dotenv`` استفاده بکنیم که بعدا همه جوره به کارمون میاد
<br>
	
- با نصبش شروع میکنیم که عین بقیه پکیج هاست و فرقی نداره 
	- ``npm i dotenv``
<br>

بعد از نصب میریم سراغ ساخت یه فایل جدید توی فولدر بات به نام ``env.``
<br>
	
و دیتا هارو به صورت خیلی ساده توی فایل تعریف میکنیم من الان فقط 3 تا پارامتر نیاز دارم 
<br>

<div dir="ltr">

```
TOKEN=ODJ3MDk4jgxNzWjE1BDU0.YI.xksnks77ebvqEY1Rk4YU_2YwE_Tyo
CLIENT_ID=837097281712415454
GUILD_ID=763773694542126274
```
</div>

<br>
	
بعد از نوشتن این 3 تا مغیر فایل رو ذخیره میکنیم و میریم سراغ فایل ``register-command.js`` تا یکمی عوضش کنیم
<br>

<div dir="ltr">

```javascript
const { REST } = require('@discordjs/rest');
const { Routes } = require('discord-api-types/v9');
// ezafe kardn [dotenv] be file
require("dotenv").config();

// daryaft data ha az file [.env]
let clientID = process.env.CLIENT_ID
let token = process.env.TOKEN
let guildID = process.env.GUILD_ID



const commands = [{
  name: 'ping',
  description: 'in command dar javab mige [Pong!] :)'
}]; 

const rest = new REST({ version: '9' }).setToken(token);

(async () => {
  try {
    console.log('dar hal ezafe kardn (/) command');

    await rest.put(
      Routes.applicationGuildCommands(clientID, guildID),
      { body: commands },
    );
      // for global register 
      // await rest.put(Routes.applicationCommands(CLIENT_ID),{ body: commands },);

    console.log('(/) command be server ezafe shod!');
  } catch (error) {
    console.error(error);
  }
})();
```

</div>
<br>

با تغیراتی که توی کد بالا به وجود اوردیم دیگه دیتا ها از فایل ``env.`` گرفته میشه و دیگه نیازی نیست توی فایل اصلی تعریفشون کنیم
<br>

**حالا نوبت فایل ``bot.js`` هستش که باید بهینه بشه**
<br>

جدا از اینکه باید متغیر توکن رو از  دیگه از فایل ``env.`` داخلش قرار بدیم باید دستورات بات رو هم به یک فولدر و فایل های جدا انتقال بدیم
<br>

دلیلش هم اینه که فرض کنید شما یه بات دارید با بیش از 50 تا دستور و اگه قصد داشته باشید هر بار یکی از دستورات رو ادیت بدید کار خیلی سختی خواهد بود چون باید همش توی یه فایل بزرگ و شلوغ این ور و اون ور برید تا بتونید تیکه تیکه اون دستور رو ادیت بدید
<br>

- پس ما اینجا از یک متد به نام **کامند هندلر** استفاده میکنیم

<br>

برای شروع کار با کامند هنلدر اول نیازه که یک پوشه برای فایل های کامند ها ایجاد بکنید
<br>

پس ما به صورت خیلی ساده یه پوشه به نام ``commands`` ایجاد میکنیم
<br>

در مرحله بعد میریم سراغ ساخت فایل برای یک کامند که ما از اون جایی که توی اموزش بالا کامند پینگ رو داشتیم برای کامند پینگ یک فایل میسازیم به نام ``ping.js``
<br>

توجه داشته باشید که فایل ``ping.js`` رو توی پوشه ``commands`` قرار بدید
<br>

و بعد کد زیر رو توی فایل مینویسیم
<br>

<div dir="ltr">

```javascript
module.exports = {
	name: 'ping',
	description: 'Replies with Pong!',
	async execute(interaction) {
		await interaction.reply('man ba command handler kar mikonm va az folder ``commands`` va file ``ping.js`` miam va be shoma migam [Pong!] :)');
	},
};
```

</div>
<br>

بعد از اینکه فایل رو سیو کردیم وقتشه یه تغییر اساسی توی فایل اصلی یعنی ``bot.js`` ایجاد بکنیم
<br>

برای راحتی بهتر تمامی کد های توی فایل ``bot.js`` رو پاک کنید و با کد پایین جای گزین بکنید
<br>

<div dir="ltr">

```javascript
const { Client, Intents,Collection } = require('discord.js');
const client = new Client({ intents: [Intents.FLAGS.GUILDS] });
// [fs] baray file sync az folder [commands]
const fs = require('fs');
// dotenv baray daryaft data az config
require("dotenv").config();
// var kardn data e ke az [.env] grftim va tabdil on be variable [token]
let token = process.env.TOKEN

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.commands = new Collection();

const commandFiles = fs.readdirSync('./commands').filter(file => file.endsWith('.js'));

for (const file of commandFiles) {
	const command = require(`./commands/${file}`);
	// set a new item in the Collection
	// with the key as the command name and the value as the exported module
	client.commands.set(command.name, command);
}

client.on('interactionCreate', async interaction => {
	if (!interaction.isCommand()) return;

	if (!client.commands.has(interaction.commandName)) return;

	try {
		await client.commands.get(interaction.commandName).execute(interaction);
	} catch (error) {
		console.error(error);
		await interaction.reply({ content: 'There was an error while executing this command!', ephemeral: true });
	}
});


client.login(token);
```

</div>
<br>

بعد از اینکه کد رو عوض کردیم کافیه فقط ذخیرش بکنیم و فایل رو ران بکنیم
<br>

- ``node bot.js``
	- و دستور ``ping/`` رو درون سرور میزنیم

<br>			

<img src="https://cdn.discordapp.com/attachments/826890223916154903/875351539240271882/unknown.png" />
<br>

همونطور که میبینید ما تونستیم با موفقیت 2 تا کار خوب و مهم توی کد هامون انجام بدیم 
<br>

* **انتقال متغیر های مودرنیاز به یک فایل جدا و فراخونی اونا به درون کد های اصلی**
* **جدا کردن دستورات و اتقال اونها به یک پوشه ای جدا و فایل های جدا برای مدیریت و نظم بهتر**
























  
  
  
  
</div>
