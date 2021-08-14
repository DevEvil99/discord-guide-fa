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
* [Visual Studio Code](https://code.visualstudio.com/download) (**من از VSCODE استفاده میکنم شما هرچی راحت تر هستید استفاده کنید**)
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

# ❕ چطور یک ربات بسازیم

**خیلی ساده میتونید برید به لینک زیر توی دیسکوردتون لوگین کنید و بعدش یه اپیلیکشن جدید به وجود بیارید بعدش میرید قسمت بات  اون اپلیکیشن و یه بات میسازید**

https://discord.com/developers/applications

https://user-images.githubusercontent.com/69610848/129358846-621efb3a-0889-45a1-b270-f174f1f82bd6.mp4


# ❕چطور رباتی که ساختیم رو به سرور خودمون اضافه بکنیم

**کافیه برید به دولوپر پورتال و توی اپلیکشنی که از قبل ساختید و قسمت OAuth2 و یه لینک بسازید که هم ربات به همراه دسترسی کامل رو به سرور شما دعوت میکنه هم دسترسی اسلش کامند رو برای استفاده اسلش کامند در سرور رو داشته باشه**

https://user-images.githubusercontent.com/69610848/129366135-142aee6a-1a22-4353-877c-816278c019af.mp4


- و یک نکته هم اینجا هست اینه که اگه میخاید کسی بجز شما نتونه ربات شما رو به سرورش دعوت بکنه باید برید توی ستینگ اپلیکیشن قسمت بات و اونجا گزینه ``Public Bot`` رو غیرفعال بکنید

<img src="https://cdn.discordapp.com/attachments/826890223916154903/875752488643469312/unknown.png" />	
<img src="https://cdn.discordapp.com/attachments/826890223916154903/875752208438804550/public-bot.png" />


# 📑 چه چیزایی رو باید نصب کنیم؟

- **اول از نصب ``node.js`` شروع میکنیم**
	- کافیه برید توی لینک زیر و یک ورژن که بالای ``16`` هستش رو بر اساس پلتفرم خودتون دانلود کنید و نصب کنید
	- https://nodejs.org/en/download/releases/
	- (تا اونجایی که من اطلاع دارم node.js از ورژن 13 به بعد دیگه روی ویندوز 7 نصب نمیشه!)❗
<br>

- **بعد از node.js میریم سراغ ادیتور که من خودم از ``vscode`` استفاده میکنم حالا شما میتونید ادیتور های دیگه هم استفاده بکنید مثل ``sublimeTEXT`` و یا ``notepad++``
	- https://code.visualstudio.com/download

- **بعد از نصب ادیتور میرسیم به نصب پکیج های ``npm`` که خیلی اصلی و مهم هستن**
	- برای نصب پکیج یک فولدر برای پروژه میسازیم که اونجا پکیج هارو نصب بکنیم و فایل هارو  بزاریم
	- بعد از ساخت فولدر کافیه یه ترمینال از اون پوشه باز بکنیم که شروع کنیم به نصب کامند ها که خب این توی ``vscode`` خیلی راحته
	- ``npm install discord.js @discordjs/rest discord-api-types``
	- در واقع ما با استفاده از دستور بالا 3 عدد پکیج اصلی که بهشون نیاز داریم رو نصب میکنیم
	
https://user-images.githubusercontent.com/69610848/129415347-6337ee72-266b-4b6f-9dd4-061201de78b1.mp4

- **اگر هم ادیتوری که استفاده میکنید ترمینال نداره میتونید خیلی راحت از توی خوده پوشه یدونه باز بکنید و پکیج ها رو نصب بکنید**
	
https://user-images.githubusercontent.com/69610848/129415975-1ddb8407-cb78-4822-9cf5-34f8dd115ce7.mp4

# 👨‍💻 ساخت اولین کامند

- ❕ **یادت باشه**
	- ما الان میخایم از یه پکیج به نام ``discord.js`` استفاده بکنیم که لینکش توی لیست پیش نیاز های بالا هست
	- توجه داشته باشید که حتما ``node.js`` رو نصب کرده باشید و ورژن اون بالای 16 باشه
	- در این اموزش زیاد با واژه ای ``guild`` رو به روی میشید که در واقع همون معنای سرور رو میده ``server``

<br>
<br>

🔵استاندارد ترین روش برای ساخت یک کامند در دیسکورد جی اس با اسلش کامند هستش که اول باید یه کامند رو برای بات ریجستر بکنیم
<br>
<br>
<br>
**2 نوع اسلش کامند وجود داره**


* guild command / کامند برای یک سرور


* global command / کامند برای بات که به صورت کلی هست

ما با نوع اول شروع میکنیم که هم سریع تره هم برای توسعه بهتره
<br>
برای ساخت کافیه یک فایل بسازید به نام ``register-command.js``
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

- 🔴 **یه نکته هم اینجا وجود داره و لازمه که بگم اینه که این فایل نقش بات رو نداره و فقط یبار بر اون اساسی که میخاید کانفیگ میکنید و ران میکنید و کامند رو اضافه میکنه همین!**

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

# ⚪ Ephemeral Message

- ⚪ **بعضی مواقع هم شاید دوست نداشته باشید چت با پیام بات شلوغ بشه و اون پیام رو فقط استفاده کننده ببینه و موقع باشه**

<div dir="ltr">
	
```javascript
await interaction.reply({ content: 'Pong!', ephemeral: true });
```

</div>

- فقط کافیه خط ارسال مسیج رو با اون این خط عوض بکنید و یه ephemeral بهش اضافه بکنید و اونو true تعریف بکنید



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

# 📇 امبد مسیج / Embed Message
	
🔵 **امبد مسیج یه نوع پیامه ولی قشنگ تر مرتب تر و توی یک کادر قرار داره و به نظر بهتر میاد**


- خب اول از همه میایم یه اسلش کامند برای امبد مسیجی که میخایم ارسال بکنیم میسازیم

<div dir="ltr">

```javascript
const commands = [{
  name: 'embed',
  description: 'in command be ma e embed message neshon mide.'
}]; 
```

</div>

![image](https://user-images.githubusercontent.com/69610848/129449865-64ae49b2-4fe4-4a25-8030-dcabe9965989.png)

- بعد از اضافه کردن دستور میریم سراغ ساختنش
	- همون طور که میدونید فقط کافیه برید توی پوشه commands و یک فایل بسازید برای کامند که من اینجا اسم فایل رو گذاشتم ``embed.js`` شما هرچی دوست دارید بزارید
	- بعدش کافیه کد پایین رو توی فایل وارد بکنید


<div dir="ltr">

```javascript
const { MessageEmbed } = require('discord.js');

module.exports = {
    name: 'embed',
    description: 'in command be ma 1 embed neshon mide :D',
    async execute(interaction) {
				// embed
				const embed = new MessageEmbed()
                .setColor('#bd282d')
                .setTitle('be in text migan [title]')
                .setURL('https://github.com/ali0sam/discord-guide-fa')
                .setAuthor('be in text migan [author]', 'https://cdn.discordapp.com/attachments/826890223916154903/876116512803553330/AYAYA.png', 'https://github.com/')
                .setDescription('text text text text!')
                .setThumbnail('https://cdn.discordapp.com/attachments/826890223916154903/876115837013069854/SuchMeme.png')
                .addFields(
                    { name: 'Regular field title', value: 'Some value here' },
                    { name: '\u200B', value: '\u200B' }, // inja vase in fild haro ba [\u200B] por kardin chon injori 1 field khali mishe va mire badi
                    { name: 'Inline field title', value: 'Some value here', inline: true },
                    { name: 'Inline field title', value: 'Some value here', inline: true },
                )
                .addField('Inline field title', 'Some value here', true) // injori ham mitonid field tarif konid vali model bala nazm behtari dare
                .setImage('https://cdn.discordapp.com/attachments/826890223916154903/876115904038064138/Valorant_KAY-O-Trailer-1024x576.jpg')
                .setTimestamp() 
                .setFooter('Some footer text here', 'https://cdn.discordapp.com/attachments/826890223916154903/876116512803553330/AYAYA.png');


		return interaction.reply({content: 'inja ro negah kon, e embed message!', embeds: [embed] });
	},
};
```

</div>


- حالا کافیه فایل رو سیو بکنیم و ربات رو ران بکنیم
	- ``node bot.js``


https://user-images.githubusercontent.com/69610848/129451238-1d303c18-92a1-4a82-bf72-e30fa74dbc32.mp4













  
  
  
  
</div>
