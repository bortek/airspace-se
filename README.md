# Airspace SE for Xctrack/XContest

Maps on Xctrack are managed via Xcontest webpage. Here is a short guide howto update them unsing example for SE region.

This file together with extra sectors are located in the following Github repo https://github.com/bortek/airspace-se 

If you wish to make an update feel free to submit a Pull Request. I will be happy to review and update.

## Main file update
Get the main file from Glider page here at the bottom, choose TXT format.
https://www.segelflyget.se/Verksamhet/Luftrum/
Now the file needs to be converter to UTF-8. Easiest is to open it in Notepadd++ and then select Encoding->Convert to UTF-8 menu. This is important so that ÖÅÄ characters are correctly visible on the map. Save the file. 

Then go into xcontest and Swedish page. You have to have a login to that page authorized to edit specific country airspace. Log in there. 
https://airspace.xcontest.org/app/country/25

There are always one or more airspace files which are public and thus visible in the Xctrack app. Some of them do not need to be updated e.g. barkarby-gärdet. The normal bi-yearly updated file is **sverige-luftrum-YYYY-revX** which you download using the steps above.

## Procedure to update airspace
From the available menu system make Create New File , call it somehting like "sverige-luftrum-YYYY-revX". Click on that newly created file. When inside it you can now import the airspace files (TXT)using Actions->Import menu then select your file, check mark next to "Simple preprocessing" and push Import. Double check that your sector names are correctly displayed with correct characters.  

Keep such Airspace "file" in the Airspace portal for every airspace file entity that are relevant to each other since it is esierer to maintain it like this. For example one "file" for sverige-luftrum, then another for barkarby-gärdet etc. It is also possible to import multiple TXT files into one single airspace "file" but we do not have such a need at the moment.

## Changing sector color
Now you need to set the color of all W (glider) sectors to green. Do the following while in the Airspace you are editing. On the top of the table like view there are fields called GLD POWE TYPE. To the right of TYPE click on the field and select W. This will activate W filter on all sectors. Now mark all sectors at once by clicking on the checkbox mark to the left of Name field. Then click on Line Color->Solid->rgb(0,255,0) then click Set. Next click on Fill Color->Custom->rgb(0,255,0) then click Set. 

## Publishing changes
Review the changes one more time, see that everything looks OK before making it public. The procedure is first to make a new "file" publich and then make the old one non-public. Select newly updated airspace that you want to make publick then from Actions->Properties menu srite "main" in the "Auto-update layer" section and default 72:00 hours. Mark Public checkbox and push Save.

Run Xcontest on your device, see that new airspace is updated and check that it looks correct.

In case if you discover error and want to roolback to the old airspace, re-run the steps in this section and nake new airspace un-public while making the old airspace public again.


