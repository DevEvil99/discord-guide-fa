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




































  
  
  
  
</div>
