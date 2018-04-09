# Unofficial API Reference
##Updates as I find new things
**Last updated: June 21, 2015 : 12:13AM**

https://my.staples-connect.com/portal/api/

The current portal looks to be built on AngularJS with Symfony.

***

### user
**user.status** : Returns 0 when logged in ?

**user.body** : Contains user details

&nbsp;&nbsp;&nbsp;&nbsp; **user.body.familyName** : Last name of user

&nbsp;&nbsp;&nbsp;&nbsp; **user.body.givenName** : Given first? name of user

&nbsp;&nbsp;&nbsp;&nbsp; **user.body.middleName** : Middle name of user, default is null

&nbsp;&nbsp;&nbsp;&nbsp; **user.body.emailVerified** : Timestamp when email account was verified ex: *2015-04-17 00:13:44.170176 +0000*

&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress** : Contains user contact information if given

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.company** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.address2** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.stateAbbreviation** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.zipPlus4** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.city** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.address1** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.phone** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.zip** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.mobile** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.primaryAddress.country** : Default is null

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.lastLogin** : Timestamp of last login ex: *2015-06-21 04:03:02 +0000&*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.displayName** : Display name of user, mine defaulted to my email address initially (I do not know if you can change this?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.uuid** : Assuming "unique user id"

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **user.body.email** : Email of user

***
### hub
**hub.status** : Returns 0 when logged in ?

**hub.body** : Contains hub information

&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers** : Contains controller information

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.mac** : MAC Address of controller

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.altmac** : Alt MAC Address of controller? Maybe this is a masked MAC Address?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.name** : Initial name of Hub when shipped from Staples?? - NOT what the user renamed their hub to, apparently. ex: *"StaplesConnect-XXXXX"* Where X's are numbers.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.ras** : Cloud server that the hub is connected too?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.mm** : URL that points to the portal URL. ex: *https://my.staples-connect.com/portal*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.connected** : True or False. If the hub is connected and online.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.identifier** : Assuming manufatured number of hub. This number is the same number that shows in the hub.body.controllers.name.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.hwVersion** : Returns hardware version? Currently returns "40" (June 21,2015). In the web-app code there was reference that the D-link version was "40" and there could have (maybe will be?) a "Linksys" version which could return "30".

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.marketingBrandId** : Returns 0. Looks like D-link was maybe going to market the hardware to a couple different brands, and this is how they flip the naming / branding depending on which number is indicated?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.features** : Contains controllers "features"

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.features.wifi** : Returns True or False. If the controller has wifi or not.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**hub.body.controllers.features.light_color** : So far can return "green" or "blue". Green apparently for D-link and blue for Linksys. Interesting.

***
### device

**device.status** : Returns 0 when logged in ?

**device.body**

&nbsp;&nbsp;&nbsp;&nbsp;**device.body.devices** : Returns array for each device in account

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**device.body.devices.deviceGuid** : Returns device GUID

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**device.body.devices.lastAccess** : Returns last device access to hub ex: *2015-06-19 23:46:20*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**device.body.devices.description** : Description of device as named from the device. E.g. "Tony's iPhone"

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**device.body.devices.authorized** : Returns True or False.



