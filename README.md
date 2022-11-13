# Schematics-Monitor
![schematicsBank](https://user-images.githubusercontent.com/73749151/201515586-c2f3ea23-85ce-49ca-b422-88b6bad75da7.jpg)

Instalation:
1. Place Programable Board
2. Copy code from [HERE](https://raw.githubusercontent.com/GcGoat/Schematics-Monitor/main/LUA) and paste it into board by Right mouse click -> Advanced -> Paste Lua Configuration from Clipboard
3. Connect PB to screen and container

Extra:
You can have multiple screens by simply linking more than one screen to PB. 
By default script will only show first page on all linked screens, to get second page you will need to go into buld mode, right click screen and rename it to **Screen_2**

Aditional information:
You can prioritize schematics which will be shown as orange when amount is lower than 100%, this is to simply for regular users to know which ones needs to be printed and which ones are not that important.

Just keep in mind that container contents can only be updated every 30 seconds PER core. So if you have multiple scripts scanning containers then it might take some extra time for contents to be updated. Soonest update will be indicated with a timer on top left corner
