# Assetto Corsa No Hesi - Server Files
 Server files for Assetto Corsa No Hesi Server - Dense Traffic. Posted here so you do not have to go through the struggle of configurating it yourself. Some modded cars may contain DLC content.

## Install these frameworks (Windows)
[.NET SDK 7.0.100](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-7.0.100-windows-x64-installer)

[.NET Core Runtime 7.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-7.0.0-windows-x64-installer)

[.NET Desktop Runtime 7.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-7.0.0-windows-x64-installer)

[.NET Runtime 7.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-7.0.0-windows-x64-installer)

[.NET SDK 6.0.100](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-6.0.100-windows-x64-installer)

[.NET Core Runtime 6.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-6.0.0-windows-x64-installer)

[.NET Desktop Runtime 6.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-6.0.0-windows-x64-installer)

[.NET Runtime 6.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-6.0.0-windows-x64-installer)

## Install Instructions
1. Install all the relevant frameworks.
2. Port forward
   1. HTTP Port 8081 TCP ONLY
   2. Server Port 9600 TCP & UDP
3. Extract contents into a folder
4. Double click on 'AssettoServer.exe' to run it.
5. Make sure you and your friends have all the mods (Cars & Track, CSP (Min Build 2144, Version 0.1.79), etc) required.
6. Enjoy the No Hesi Server with your friends.

## Trouble Shooting Steps
Follow these steps if 'AssettoServer.exe' does not open:
1. Open 'Event Viewer'.
2. Expand 'Windows Logs' on the left.
4. Go into 'Application' under 'Windows Logs'.
5. Within 'Actions' (right hand side of the window) click on 'Filter Current Log'.
6. Expand 'Event Sources'.
7. Select these following options
   1. .Net Runtime
   2. .Net Runtime Optimization Service
8. Press 'OK' at the bottom of the window.
9. Preview logs and see what is going wrong.
10. Use Google if you do not understand them B)

Follow these steps for any other issues:
1. Go into the 'logs' files.
2. Open the most recent log and scroll down to the bottom.
3. Look for any errors that have appeared.
4. Google them if you do not understand them B)

Follow these steps if you do not have a DLC car:
1. Go into '/steamapps/common/assettocorsa/content/cars/[insert missing car name here]'.
2. Replace the 'collider.kn5' file with a 'collider.kn5' file from a non DLC car, it does not matter what car it is.

## Mods List
1. TBC

## Modifying The Server
Follow these steps to add a modded car:
1. Find a car you want to add inside your game content folder e.g. '/steamapps/common/assettocorsa/content/cars/[insert missing car name here]'.
2. Copy it into the cars folder inside your content folder within the server files e.g. 'ServerNoHesi\content\cars'.
3. Copy the folder name of the car.
4. Open up 'server_cfg.ini' inside the 'cfg' folder of your server.
5. Find line 22 (CARS=[Insert Cars Here]).
6. Add a semi-colon (;) to the end of the string, then insert the folder name of the modded car afterwards & save the file.
7. Open up 'entry_list.ini' inside the 'cfg' folder of your server.
8. Add any amount of entries for the modded car.
   e.g. <br /> `[CAR_[Insert Number Here (Make sure you do not have the same number used already anywhere inside the file)]]` <br />
         `MODEL=[Folder Name of the car]` <br />
         `SKIN=generated/ADAn` <br />
         `SPECTATOR_MODE=0` <br />
         `DRIVERNAME=` <br />
         `TEAM=` <br />
         `GUID=` <br />
         `BALLAST=0` <br />
         `RESTRICTOR=0` <br />
9. If you would like it to be a:
    1. Car you or your friends would like to drive press 'enter' to create a new line after `RESTRICTOR=0` and type in `AI=none`.
    2. Car for AI traffic press 'enter' to create a new line after `RESTRICTOR=0` and type in `AI=fixed`. 

Follow these steps to remove a modded car (any type: AI, Personal use, etc, does not matter):
1. Open up 'server_cfg.ini' inside the 'cfg' folder of your server.
2. Find line 22 (CARS=[Insert Cars Here]).
3. Remove the name of the car from the string of text & save the file.
4. Open up 'entry_list.ini' inside the 'cfg' folder of your server.
5. Remove any entries that contain the model of the car you just deleted & save.

