Highlight Management Script goes beyond KVIrc's basic highlighting functionality allowing you to prevent all highlights from particular channels and/or nicks, along with a new highlight log window and the ability to log to file. Normal highlight configuration is done in the usual way, this script basically adds a blacklist on top.

Last updated on 5.10.16 for v1.4.


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

The 'Scripts' menu is created on the main KVIrc menubar, which then hosts the Highlight Management Script menu. Here you can turn the script on/off, list, add and remove blacklisted channels, usernames and nicks (normally you would do this via right-clicking the channel/nick directly), and configure the Highlight Log Window:

![Script configuration](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/script-configuration.png?raw=true)

The nick blacklisting dialog:

![Add nick to highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/add-nick-to-highlight-blacklist-dialog.png?raw=true)

The 'Network' entry is the name of the relevant network - if you don't know this off-hand, use the following command in a window associated with the server:

    /echo $context.networkName

Deletion of nick from blacklist dialog:

![Delete nick from highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/delete-nick-from-highlight-blacklist-dialog.png?raw=true)

Select the relevant network at the top, then the nick at the bottom, then press OK.

Username blacklisting dialog:

Blacklisting on a nick isn't good enough when a user continuously changes their name (e.g. some of the newer commit bots) - in this case the username probably remains constant, so you can blacklist on that.

In the example of a user with the full usermask 'Not-bb4!~notifico@198.199.82.216', the user's nick is 'Not-bb4', and their username is '~notifico'. The tilde at the front is part of the username, and is prepended by the server when the user doesn't run a reachable ident service on their machine (which will be almost every real remote user, since its obsolescent).

![Add username to highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/add-username-to-highlight-blacklist-dialog.png?raw=true)

This dialog works in the same way as the nick blacklisting dialog.

Deletion of username from blacklist dialog:

![Delete username from highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/delete-username-from-highlight-blacklist-dialog.png?raw=true)

This dialog works in the same way as the deletion of nick from blacklist dialog.

Channel blacklisting dialog:

![Add channel to highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/add-channel-to-highlight-blacklist-dialog.png?raw=true)

This dialog works in the same way as the nick blacklisting dialog.

Deletion of channel from blacklist dialog:

![Delete channel from highlight blacklist dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/delete-channel-from-highlight-blacklist-dialog.png?raw=true)

This dialog works in the same way as the deletion of nick from blacklist dialog.

Listing blacklisted nicks, usernames and channels outputs them as text to the current window.

'Configure Highlight Log Window...' (discussed later) shows the following dialog:

![Highlight Log Window configuration dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/highlight-log-window-configuration-dialog.png?raw=true)

The dialog already comes with notes, but for convenience [here is the $date function documentation](http://www.kvirc.net/doc/fnc_date.html), and the directory used to log highlights can be found in the main KVIrc configuration under IRC -> Tools -> Logging -> 'Save logs to folder'. Currently the following is used as the log filename:

    Highlight Log - <yy>-<mm>-<dd>.txt


Channel And Nick Menu Integration
=================================

Normally to add or remove nicks, usernames and channels from the blacklist, you will use the integrated menus - right-click the channel to get at the channel menu:

![Channel menu - blacklist channel](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/blacklist-channel-channel-menu.png?raw=true)

Right-click a nick to get at the nick menu:

![Nick menu - blacklist nick](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/blacklist-nick-nick-menu.png?raw=true)

The following notes dialog appears to allow you to optionally note your blacklist reasons in case you forget in the future:

![Blacklist nick notes dialog](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/blacklist-nick-notes-dialog.png?raw=true)


Highlight Log Window
====================

On starting the script up, the 'Highlight Log' window appears usually at the bottom of your window list. The following is an example of two highlights, one from a channel and one from a PM, with the default output configuration:

![Highlight Log Window](https://github.com/OmegaPhil/kvirc-highlight-management-script/blob/master/doc/highlight-log-window.png?raw=true)

See under 'General Configuration' above for how to customise the output, and where the highlights are logged to file.


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

OmegaPhil@startmail.com
