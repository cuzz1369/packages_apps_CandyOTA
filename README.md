# CandyOTA

# Requirements for CandyOTA to work properly...


1. Device must have offical support by CandRom's
2. Dircet linking 
3. A brain

# OTA XML 
Edit these files to match your own device 
``` XML
<?xml version="1.0" encoding="UTF-8"?>
<ROM>
	<!--ROM name-->
		<RomName>Candy5</RomName>

	<!--NEED EDIT EVERY NEW UPDATE-->
		<VersionName>candy5-Release.v1.5.0-20150310-OFFICIAL-d2att</VersionName>

	<!--NEED EDIT EVERY NEW UPDATE-->
		<VersionNumber type="integer">20150519</VersionNumber>

	<!--NEED EDIT EVERY NEW UPDATE-->
		<DirectUrl>DIRECT LINKS HERE</DirectUrl>

	<!--Dont Touch This K!-->
		<HttpUrl nil="true" />

	<!--CandyRoms Version-->
		<Android>1.0.1</Android>

	<!--NEED EDIT EVERY NEW UPDATE-->
	<!-- You can disable MD5 checking like this: <CheckMD5 nil="true" />-->
		<CheckMD5>MD5 HERE</CheckMD5>

	<!--THIS NEEDS TO BE EDITED EVERY NEW UPDATE-->
	<!--Please enter this in BYTES only.Otherwise an incorrect value will be shown-->
	<!--Use google to get the byte vale ex 214.17 mb to bytes-->
		<FileSize type="integer">214170000</FileSize>

	<!--Maintainer handle-->
		<Developer>Flashalot</Developer>

	<!--The one and only Candy website-->
		<WebsiteURL>http://the-candy-shop.co/</WebsiteURL>

	<!-- Team donate link (fyi its one big troll og candy users will rember it) -->
		<DonateURL>https://goo.gl/g9w6ui</DonateURL>

	<!--Changelog here... Use DaringFireball's Markdown to format it-->
	<!--Surround special characters with the CDATA tags or your XML will NOT parse-->
		<Changelog>
		### Changelog 20150105
		* Stuff
		* Updated this, or that
		* Fixed all the things
		* We even fixed this
		* Don't forget all the awesome features you added
		</Changelog>

	<!--Default Candy addons page. Don't like it change it! -->
		<AddonCount>2</AddonCount>
		<AddonsURL>https://basketbuild.com/uploads/devs/Flashalot/addons.xml</AddonsURL>

</ROM>
```
Once you're done with that save it as ota.xml and upload it to your host
and add it to your ro.ota.manifest="link here to your ota.xml" 

##Updates

Now that you have that done whenever you want to push update make sure to do this on ever update 

- look at your build.prop so that your version is incrementally higher than before

```
  # Before
  ro.candyroms.version=20150105
  
  # After
  ro.candyroms.version=20150108 
```
- Replace/overwrite your ota.xml with the candyversion number you saw in the zip

- Publish your ROM on your favourite website

Now all your users will get an OTA update notification at some point, whenever their device checks for one!


# Licensing

This project is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0). A copy of the licence can be obtained [here](http://creativecommons.org/licenses/by-nc-sa/4.0/legalcode).

This licence is chosen because it gives people the rights to clone this project and freely use it in their ROM or application, but only so long as they are sharing it in the same manner, and not going to publish it for commercial uses. I.E. This is free to use and modify (so long as you share any changes under the same licence), but you can't take it and sell it.

Other parts of this project (Bypass, cardsview) have their own licences and are not affected by this one.
