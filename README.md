# Account Details Roundcube Plugins

This is a fork from Gene's original plugin.  Changes herein:
 - Call out the user's WAN IP address in the "User Info" section instead of the server IP address; changed line 174 in account_details.php
 - My folders are created as Top Folders, not sub-folders of INBOX; changes to lines 214,218, 222, 226, 230 in account_details.php 
 - Changed "Mailbox Details" to "User System Mailbox Details"; line 57 of localization/en_US.inc

-----

I have merged 3 plugins, userinfo, moreuserinfo and serverinfo into one .. 

Account Details Plugin for Roundcube

Adds tab in Setting for more user info. 
* Identities
* email address
* storage space quota
* Operating System
* Web Browser
* Video Resolution
* Mailbox Stats
* Server URL, port and other useful info
* CalDAV URL;s
* CardDAV URL's
* and more
You can enable/disable certain things via the config.inc.php

Installation
-------------
Upload contents to '/roundcube_location/plugins/account_details/'.

Copy folder named 'copy_to_web_root' into your webroot. Basically want your url like 'http(s):domain.ltd/tutorials/etc/'
I just have empty html index files. You can customized your tutorials to suit your needs and custom to your services.

Enable plugin via config.inc.php with

$config['plugins'] = array('account_details');

Make an hourly cronjob with your web credentials as follows for Roundcube Version Checking:

`curl https://api.github.com/repos/roundcube/roundcubemail/releases | grep tag_name | grep -o "[0-9].[0-9].[0-9]\{1,\}" | sort -n | tail -1 > /path_to_roundcube/plugins/account_details/rc_latest.txt`


Enjoy!

Screenshots
-----------
With All Details enabled

![Alt text](/tests/ad-screenshot1.png?raw=true "Account Details Screenshot")

More to come
