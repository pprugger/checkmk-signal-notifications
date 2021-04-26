# Signal notifications for checkmk

This checkmk plugin enables your checkmk server to send notifications via Signal.
At the moment there is no support for signal groups.

This plugin requires the following python libraries:
* dateutil
* datetime
* pysignald
* phonenumbers

Python3 is required.

This plugin uses signald for the communication with Signal.
For the documentation of signald see:
https://gitlab.com/signald/signald

## Installation
* Install signald on your server liked described here:
https://signald.org/articles/getting-started/

* Register a new signal account or link signald with an existing account
* Install the python libraries
* Copy this script to /omd/sites/<YOUR-SITE>/share/check_mk/notifications
* Change from_number in the script to your signal account number
