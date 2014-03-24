Highlight Management Script goes beyond KVIrc's basic highlighting functionality allowing you to prevent all highlights from particular channels and/or nicks. Normal highlight configuration is done in the usual way, this script basically adds a blacklist on top.

Last updated on 24.03.14 for v1.2.


Installation
============

To load the script into KVIrc (which then persists until you uninstall) and run its startup alias, in a KVIrc console window:

    /parse <path to script file, speechmark-delimited if the path contains spaces>
    /HighlightManagementScript::Startup

Once the script is installed, HighlightManagementScript::Startup is automatically called when KVIrc is started.


Dependencies
============

None.


Uninstallation
==============

In a KVIrc console window:

    /HighlightManagementScript::uninstall::uninstall


General Configuration
=====================

The 'Scripts' menu is created on the main KVIrc menubar, which then hosts the Highlight Management Script menu. Here you can turn the script on/off, list, add and remove blacklisted channels and nicks (normally you would do this via right-clicking the channel/nick directly):

![Script configuration](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7367/script-configuration.png)

The nick blacklisting dialog:

![Add nick to highlight blacklist dialog](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7388/add-nick-to-highlight-blacklist-dialog.png)

The 'Network' entry is the name of the relevant network - if you don't know this off-hand, use the following command in a window associated with the server:

    /echo $context.networkName

Deletion of nick from blacklist dialog:

![Delete nick from highlight blacklist dialog](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7389/delete-nick-from-highlight-blacklist-dialog.png)

Select the relevant network at the top, then the nick at the bottom, then press OK.

Channel blacklisting dialog:

![Add channel to highlight blacklist dialog](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7390/add-channel-to-highlight-blacklist-dialog.png)

This dialog works in the same way as the nick blacklisting dialog.

Deletion of channel from blacklist dialog:

![Delete channel from highlight blacklist dialog](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7391/delete-channel-from-highlight-blacklist-dialog.png)

This dialog works in the same way as the deletion of nick from blacklist dialog.

Listing blacklisted nicks and channels outputs them as text to the current window.


Channel And Nick Menu Integration
=================================

Normally to add or remove nicks and channels from the blacklist, you will use the integrated menus - right-click the channel to get at the channel menu:

![Channel menu - blacklist channel](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7392/blacklist-channel-channel-menu.png)

Right-click a nick to get at the nick menu:

![Nick menu - blacklist nick](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7393/blacklist-nick-nick-menu.png)

The following notes dialog appears to allow you to optionally note your blacklist reasons in case you forget in the future:

![B](https://f92fac806bf10a96c0b8-8a0a46e5f1a5cc9854958bc3503f0f88.ssl.cf1.rackcdn.com/media_entries/7394/blacklist-nick-notes-dialog.png)


Alias/Scripting Usage
=====================

The script is fully commented so should be fairly accessible for those wanting to see how to take its use further - for alias usage, see comments preceeding the alias, or run the alias without parameters for help/errors.


Development
===========

Try out my modification of the [geany](http://www.geany.org/) IDE, extending it to syntax highlight, parse KVIrc Script for aliases, events, variables, shortcut for loading scripts into KVIrc etc: [Github documentation](https://github.com/OmegaPhil/geany-kvircscript/wiki/README---KVIrc-Script-Integration).


Bugs And Feature Requests
=========================

Please create an issue on the [Github issue tracker](https://github.com/OmegaPhil/kvirc-highlight-management-script/issues).


Contact Details
===============

OmegaPhil+KVIrc.Script@gmail.com
