# Signal notifications for checkmk

This checkmk plugin enables your checkmk server to send notifications via Signal.
At the moment there is no support for signal groups.

This plugin requires the following python libraries:
* pysignald
* phonenumbers

Python3 is required.

This plugin uses signald for the communication with Signal.
For the documentation of signald see:
https://gitlab.com/signald/signald

# Pull Requests
If you find errors in the script, feel free to create pull requests.

# Installation
* Install signald on your server liked described here:
https://signald.org/articles/getting-started/

* Register a new signal account or link signald with an existing account
* Install the python libraries
* Copy this script to /omd/sites/YOUR-SITE/share/check_mk/notifications
* Ensure the script is executable
* Change from_number in the script to your signal account number
* Add a new notification rule, the number of the recipient is passed as a number in E164 format for example: +123456789

![Rule](/notification_rule.PNG)


Here is an example of a signal message, part of the data obfuscated for privacy reasons:


![Example](/example.png)


Thanks to mh-g who brought me to the idea!

Code to be found here:

https://github.com/mh-g/check-mk_signal-cli


# License 
This project is licensed under the MIT license. See the [LICENSE](LICENSE) for details.


