# Sigma ROX 11.1

## The good
Color is used to highlight parameters onscreen. Brilliant idea.
Display is easily legible even in direct sunlight. 

## The bad
Incomplete `.fit` supoprt. No HR zones, no lap button press. HR zones not detected in workouts, HR zone can't be displayed onscreen. 
Annoying messages: `Searching…` GPS fix message keeps onscreen, `Sync. in progress` appears randomly.

## The ugly
Low-quality fonts
Unrefined beep sound
Switching on/off takes way too long
Marketing photos are misleading - display isn't nearly that good and crisp.

----

## Bugs

## Incomplete .fit support
### HR zone targets not recognized in workouts
I've got a dozen workouts from my Garmin that use HR zones as targets. Those are valid `.fit` files created with either Garmin unit or Garmin Connect service. However when imported to Sigma app or copied directly to ROX 11.1 heart rate zones aren't recognised as a target.
Those blue and orange colors of workout phases are read from `intensity` values within `.fit` file. Heart rate zones are displayed as target values in phases description. But those zones aren't converted into actual HR values that are used as target intervals during workout.
Garmin FIT SDK states that `target zones represent target limits that have already been established through other means, such as in a settings file, through a user interface, or predefined on fitness equipment. If zones are predefined their numbering should start at 1 (since 0 is reserved to indicate a custom zone).` 
But the only way to make a HR target with Sigma is by setting `target_hr_zone` to `0` and calculate and specify `custom_target_heart_rate_low` and `custom_target_heart_rate_high` values manually.

### Lap button press not supported 
Lap button press is not recognised as a valid workout step termination trigger. 

## Annoyances

### Low-quality font
That's the first thing you'll notice when you start the ROX 11.1. Marketing pictures are misleading, the display itself and symbols on it are simply not pleasant to look at.
It's very good that the unit uses a non-aliased font, it's crisp and sharp. But this only works when it's a quality font. The one used on Rox 11.1 is just so badly made. 
For example, the message that appears during power off has a crooked 'B' in 'Good Bye'. 'B', 's', 'k', 'v', bluetooth symbol - everything seems uneven, with vairable width and of different density.
Another example: 'Settings' menu header. 't' is 3px wide, 'n' also has 3px wide legs, but 'i' is 4px wide, as well as 'g'.
Large '6' is 1px short on the top compared to other digits.

### Initial GPS fix message
`Searching...` message is displayed forever until GPS fix is acquired and one can't get rid of it. It briefly goes away after pressing `+` or `-` button  but reappears in a couple of seconds.
Expected behaviour should be this message going away `+` or `-` button is pressed and should only reappear as `GPS OK!` once fix is aquired.
For now (as of V2.14) It's a VERY annoying behaviour. I literally was riding one day for almost an hour and could not see half of the screen. 

### Syncing message
`Syncing` message appears every now and then for no reason in workout mode. It does nothing but produces a distraction and hides training data from view. 
Expected behaviour would be no message at all or a small circular arrows icon in the corner.

### Power on/off takes a way too long press
You should hold Power button for 3 seconds to turn the unit on or off. That's about 1 sec. longer than one is expecting. 

### Unpleasant beep sound
Beep sound has artefacts. Instead of a distinct beep it's more like an unpleasant tinkling sound. This may be the beeper itself or the sound coded in firmware.

## Missing features
### Heart rate zones. 
It seems to be related to HR zones bug. Sigma can't display HR zone on the display - there's no such option in under `Heart rate` values list.

### HR (intensity) zones calculation
HR (intensity) zones are set per sport profile and are measured in %. It appears that it's % of max HR, but it's not specified anywhere. 
There should also be a possibility to specify resting heart rate and calculate and use zones based on % of HR reserve (HRmax - HRrest = HRreserve).

## Unspecified
The manual doesn't mention how to connect the unit to PC/Mac. Simply plugging in a USB cable won't work, you have to press all the five buttons at once and select connection mode.