## Detect user's country in Qt
When we talk about country we do mean the country set in user Preferences (OS X), Control Panel (Windows). This is the country that user selects when performing the first OS installation.  `QLocale::system()` often fails here thus the provided function `QLocale::Country detectUserCountry()` has special handling on OS X and Windows. You're free to add custom handling for other OS that Qt supports.

##### `detectUserCountry` gets country on OS X as set in Preferences under *Region*:
![OS X Region in Preferences](/images/region_mac.png)

##### `detectUserCountry` gets country on Windows as set in Control Panel under *Location*:
![Windows Location in Control Panel](/images/location_win.png)
