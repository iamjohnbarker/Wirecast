This is a forked and tweaked version of netnutmike's work on the Applescript for linking Wirecast with a Korg nanoKONTROL2 device.

The main tweaks in my version is to allow for custom naming of shots within Wirecast

##Setup
Download (MidiPipe)[http://www.subtlesoft.square7.net/MidiPipe.html].

You'll also need SampleLayout.nktrl2_data within this repo. Download it and write it onto your device.

##MidiPipe
Open it up and create a pipe like the example below:

IMAGE

###Midi In
Your Korg nanoKONTROL2 device should appear in the dropdown list within Midi In as one of the inputs - be sure to select it.

###A List
This should be okay when left as the defaults (everything checked).

###AppleScript Trigger
For the AppleScript Trigger, copy and paste the contents of "AppleScript Trigger.txt" into the text field.

You should see a "Not complied" message, which can be easily fixed by pressing any button on our Korg nanoKONTROL2 device. The message should change to "Compiled".

##Shot names
There are two placed that you will need to set custom names for your shots, one is within the "AppleScript Trigger.txt" file you already downloaded and the other is in Wirecast (but we'll get to that later).

For now, I've set the custom names to as follows:
- CamName1, CamName2, CamName3, CamName4, CamName5, CamName6, CamName7, CamName8
- LowerThird1, LowerThird2, LowerThird3, LowerThird4, LowerThird5, LowerThird6, LowerThird7, LowerThird8

###Editing the names
Open up "AppleScript Trigger.txt" in your favourite editor and do a find and replace for each of the names you want to change.

For example, if you want "CamName1" to be "Wide Shot", make that change everywhere you see "CamName1" within the "AppleScript Trigger.txt" file.

Important: You'll need to then Copy>Paste that file into the AppleScript Trigger in MidiPipe!

Do the same for Lower Thirds, if you want to use them. "LowerThird1" might become "Event Title".

##Wirecast
Open up your version of Wirecast (this has been tested with 6 and 7 and works great).

###Shot names
This is the other place that shot names are very important - You'll also have to add " cam" after each of your main camera shots (on Master Layer 3).

For example, if you originally changed "CamName1" to "Wide Shot" in the AppleScript, you should now rename the shot within Wirecast to "Wide Shot cam".

For Lower Thirds, you might have changed "LowerThird1" to "Event Title", you'll need to rename it in Wirecast to "Event Title l3rd"

Adding the " cam" and " l3rd" just means you can have the same name for both shots, but they won't conflict and have odd results.

###Intro/Outro
I've also added the ability to cue up an Intro or Outro video within Wirecast which will play with you hit Take/Go.

These videos should be imported as a normal shot and placed on Master Layer 1 and simply named "intro" or "outro" as approriate.

They'll play by hitting the "Marker Left" or "Marker Right" buttons on your nanoKONTROL2.
