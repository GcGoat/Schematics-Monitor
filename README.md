# Schematics-Monitor
![schematicsBank1 2](https://user-images.githubusercontent.com/73749151/222956951-1235097e-2694-4621-923c-3cfe213657f0.jpg)
![schematicsBank1 3](https://user-images.githubusercontent.com/73749151/222972048-37fb823b-c87a-485a-8bd1-1ff88d3afe9a.jpg)

Instalation:
1. Place Programable Board
2. Copy code from [HERE](https://raw.githubusercontent.com/GcGoat/Schematics-Monitor/main/LUA) and paste it into board by Right mouse click -> Advanced -> Paste Lua Configuration from Clipboard
3. Connect PB to CONTAINER FIRST and then to screen(s). 

MAIN THING is to link container to the first slot which contains needed event listeners. Rest 9 slots can be used for 9 screens. 

Screen can be in vertical or horizontal position. Its state will automatically update depending on how you place monitor. Horizontal monitor will contain all 3 pages on one screen, while vertical one will contain only one page per screen.

Extra:
You can have multiple screens by simply linking more than one screen to PB. 
By default script will only show first page on all linked screens, to get second page you will need to go into build mode, right click screen and rename it to **Screen_2** or **Screen_3**

Aditional information:
You can prioritize schematics which will be shown as orange when amount is lower than 100%, this to be more obvious for regular users to know which ones needs to be printed and which ones are not that important. This needs to be done by directly editing code, was to lazy to add exported variable for each of them. Its straight forward way, just add "true" for schematics you want to prioritize as some existing examples in default setup.
Aditionally you can set schematic to "false" which will set schematic to low priority. 
High priority schematics name turn white when amount is equal or over 100%, normal priority schematics will turn grey when there is enough of those. Low priority remains grey at all times.
Tile and sub borders will turn red in case linked schematics container isint set to be used as main for entire core. This can be disabled in LUA parameters window

Just keep in mind that container contents can only be updated every 30 seconds PER player. So if you have multiple scripts scanning containers then it might take some extra time for contents to be updated. Soonest update will be indicated with a timer on top left corner.
Running it for the first time, nothing will appear on screen(s) until container content scan is performed, which can be delayed due to previously mentioned limitations. 
