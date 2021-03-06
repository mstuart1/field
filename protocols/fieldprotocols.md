# Philippines Field Protocols
Michelle Stuart  
6/7/2017  



#### Mayoral Visits and University President Courtesy call

The first full day in Leyte, visit the Mayors offices of Albuera and Baybay.  If the PIC forms still need to be signed, bring those along.  Also take a photo of researcher with the office staff to document the visit.  

Email the university president before departing the US to arrange a courtesy call for the same day.

#### Standard dive gear
For each diver pack:

* Wetsuit/diveskin
+ Fins
+ Booties
+ BC
+ Regulator
+ Weights (these can be left on the boat)
+ 1 tank per planned dive

#### HOBO retrieval and replacement

As a first dive of the season, replace the HOBO temperature data loggers at Visca.  This is a nice way to check out gear close to the marine lab and do a test dive to make sure everything is working as expected.

Before the dive,

* connect the base station to the computer
* connect the hobo to the base station
+ Open the software
+ Click “launch device” first icon on the left 
+ First device launch now and change interval to 30 minutes; 
+ second device launch on time 15 minutes later.
+ Take a screen shot of the launch.

In addition to standard dive gear, bring:

* gloves for handling hydroid covered PVC housing
+ scissors for cutting present zipties
+ launched HOBO sensors
+ fresh zipies
+ slate with paper and pencil for noting which serial number HOBO went in which location, and which was taken from which location.

The first HOBO is located just south of the resort tower at 10.74373, 124.78668.
The second HOBO is located about 10m to the SW, 10.74364, 124.78665.

Turn of the old HOBOS by clicking “read out device”.  Save the files.

Clean the old hobos by running under water and scrubbing with a test tube brush.  If they resist, let them dry out for a month or a year and try again. 

#### Drifters
Plot the deployment locations on the GPS.  In 2017 they were north, south, west, west center, center and east.

Unscrew cap to start microstar transmission, screw on drogue cap and open drogue until it clicks.

Navigate boat to deployment locataions and drop in the drifters.

#### Clownfish surveys
Team backs off until anemone surveyor has a chance to observe.

Anemone surveyor:

1. searches adjacent area for anemone tag (anemone could have moved a few feet since last encounter)
2. records time, species, size of anemone, tag number if present
3. watches anemone and counts number of fish and estimate sizes (same procedure regardless of species)
4. records spp of fish, estimate sizes
5. Adds tag after the fact if one was missing or if there was only one zip tie tag (old system tag)
6. Flags anemone with flagging tape that it is ready to be hunted if APCL were present.

Fish catcher:

1. waits for flagging tape to indicate anemone is ready for fish capture, ok to chase fish if they flee the area
2. catches all fish of desired size range and places in holding vessel adjacent to anemone
3. can move on to next anemone if anemone surveyor has flagged it

Fish processing team (2 people):
once the fish catcher has moved to the next anemone, begins processing fish in the holding vessel

1. measure the fish and photograph on the gridded slate
2. Record size and tail color
3. Scan for pit tag, if present, 
    1. record and release fish
4. If no pit tag is present, 
    1. collect fin clip and record sample id
    2. insert pit tag and record tag id
    3. release fish
5. Repeat until all fish in the vessel have been processed.
6. Move on to next holding vessel.

#### Evening data processing

1. Using forceps or a ziptie to hold the fin clip and tag in place, dump the seawater out of the vial.  Using a squeeze bottle, fill the vial with ethanol (100%) and place in a cardboard sample box.

1. Dunk the ziploc baggies containing GPS units under fresh water, then towel off to dry.  If there is a lot of sea water inside the ziploc, remove the inner aquapac and also dunk that in fresh water, or else towel dry the aquapac and remove the GPS.  Turn the ziplock inside out to dry the interior.

2. Submerge the SeaLife camera in fresh water and remove the lens cap and macro lens.  While submerged, push each button 3 times.  Remove the data plug and rub finger over the gold electrodes.  Immediately remove the camera from the fresh water bath and towel dry the data connectors.

3. Submerge dive watch in fresh water bath and push each button 3 times.

4. If the pit scanner is in the custom housing, remove the pit scanner, re-seal the housing and submerge in fresh water bath.  Push each button 3 times.  If the pit scanner is in the EWA housing, dunk the housing in fresh water, then towel dry.  Remove the aquapac and towel dry. Remove the scanner from the ziploc and inspect for any wetness (there should be none).  

5. Save the day's track on the GPS, then plug it into the computer and transfer the track to the folder corresponding to the GPS unit.  Repeat for each GPS unit.  Remove the batteries and plug them into the charger; begin charging.  Place the rear-doors of the GPS units inside the aquapac bags to prop them open to dry them out.  

6. Plug the pit scanner into its charging cord, start windows on the virtual box, plug in the USB for the pit scanner, select Prolific from the USB options on the virtual box, open the bioterm software, open a connection, turn on text capture, hit shift-G to begin downloading scanned tags.  Tags will save to the Bioterm.txt file on the desktop.  Drag the Bioterm.txt into the network connection to transfer from windows to the mac.  Plug the scanner charger in to begin charging.

7. Make sure the data connection for the camera is completely dry.  Plug the camera into the wall and choose external power from the menu. Turn on the wifi and transfer all new photos to the iphone app. Turn off the camera, turn it back on and select charge from the menu.

8. Enter datasheets into the excel spreadsheet.  Saving as csv might make using with git easier but that still hasn't been decided.

9. In RStudio, run 01checkxl.Rmd - checks for type-os in the excel spreadsheet.

10. Run 02trimgpx.Rmd - creates new track.gpx files that begin and end with survey times.  Import the trimmed tracks into QGIS as vector layers.  Save the tracks as shapefiles to be concatenated into one file at the end of the season.

11. Run 03anemstoqgis.Rmd - creates a csv/QGIS map layer containing the locations of anemones.  Import into QGIS as a delimited layer.

12. Run 04divesummary.Rmd - creates a table of fish totals for each dive and site.
