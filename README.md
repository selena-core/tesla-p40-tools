# tesla-p40-tools
Using Nvidia Tesla P40 on WDDM ezy

Use your Tesla P40 24gb on WDDM mode for any GPU task you need!

Disclaimers
1) Only for Windows Pro 10 and 11 64 bits (for the moment)
2) Nvidia Driver MUST BE EQUAL or lower than 551.61 (any new driver, WDDM is not available)
3) Multi GPU systems can have trouble choosing which GPU to be used on the program/game
4) No Virtual Display at the moment
5) Required another Device capable of display output on your system (iGPU or another Dedicated GPU)



551.61 Drivers:

Best option (Works with Tesla and Geforce GPUs as RTX and etc):
https://drive.google.com/uc?export=download&id=1r27fInHVQITd95M1mNzU9lRoRMjMLj8c


Data Center Driver:
https://drive.google.com/uc?export=download&id=15Fx7RX_anupzZYbAdDH0b_Es5LM2zEUk


Game Ready Driver:
https://drive.google.com/uc?export=download&id=1v--seHf8kj800GlpGK2mn_I2951ZhFjo




Extras:
Some games may require updated drivers to play, 
(example: Battlefield 6 requires a newer version than 551.61)
in some of these games you can trick the game to think the driver
is other version by modifying a string on the nvapi64.dll file.
(nvapi64.dll can be found at C:\Windows\System32)
(You can patch the file before install, folder inside the driver zip ./Display.Driver ,
it will give an error on install but just ignore)

I used at the time:
Verpatch - a tool to patch win32 version resources on .exe or .dll files,
Version: 1.0.15 (25-Oct-2016)
You can find a remains of it here: https://github.com/Mendeley/Update-Installer/blob/master/external/verpatch/verpatch-ReadMe.txt

For the cmd:

verpatch.exe nvapi64.dll "32.0.15.8088" /pv "32.0.15.8088"

Where "32.0.15.8088" are the strings that identify the driver
version, so u look for a version that your game works and 
copy its complete version ID and edit the cmd accordingly.

CAUTION the string text enconding (example: UTF-8 and etc)
must match the original file enconding, dont understand?
A simple ctrl+c ctrl+v maybe copy text using enconding that 
Verpatch or the game dont identify and it fail some way.

