# Cesium-SpaceNavigator
Navigate through Space at warp speed, orbit planets, fly over terrain, or take a relaxing stroll through a park.

I've created a 5DOF testapp here
hyperscripts.atspace.tv/Cesium/Apps/Sandcastle/gallery/fiveDof.html
It can take about 20-30 sec to load which might be due to the webhost or perhaps because it's using the unminified version, I'm not sure. To activate just press one of the 3Dmouse buttons.
Some important caveats, if you do any of these in Chromium in Windows (Chrome and Opera)
-reload the webpage
-minimize the browser
-switch tabs
It will lose connection to the 3DMouse and you have to close all tabs and reboot the browser to get it to work again. That's why I usually dedicate a browser (such as Opera) just for 3DMouse apps. I've reported this bug to Chromium in September 2014 but it is still present. I have not yet tested with Firefox, IE. nor Safari, but I'll try to get support for them as well in case they are not working.

Console settings (ctrl-shift-i with 3dwindow in focus)
If it's not working you can try setting controllers[0].device= to other numbers, say 0 to 5. Also to determine the proper maxInput value you can type controllers[0].showRaw=true then push max in one direction and see the max value, then type controllers[0].showRaw=false then set controllers[0].maxInput= to that value. I should probably automate this process. There's also the .scales array to reverse axis direction, and .deadZones array. I do eventually plan to have a GUI for these settings, instead of having people use the console.

There's also this page which simply changes a few of the controller's properties
hyperscripts.atspace.tv/Cesium/Apps/Sandcastle/gallery/sixDof.html
To change the movement scheme type controllers[0].scheme="string"
replace "string" with one of the following
"sixDofTrue"
"sixDofCurved"
"fiveDofCamUp"
"fiveDof"

With the five DOF options roll action on the 3DMouse controls camera FOV.