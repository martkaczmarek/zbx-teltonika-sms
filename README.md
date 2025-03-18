# zbx-teltonika-sms
Template for sending SMS messages from Zabbix with Teltonika routers.
Currently only tested with RUT240, but all the RUT- devices seem to have similar API. 

### How to use

The three parameters that need to be set are URL, Username and Password. 
You can do it by creating specified user macros or replacing the macros with literal values in media type configuration. 
URL should have the form of: `http://<IP>/cgi-bin/sms_send`

Keep in mind if you use user macros and test the media type in configuration menu, the macros will not be resolved (you need to provide real values during test). They will resolve in normal operation. 

"To" parameter (the "Send to" field in user configuration) should contain a phone number in one of two formats:
1. A local number without country code
2. A number with country code, prefixed with `00`. So, for example for Polish number that would be `0048xxxxxxxxx`. 

To set username and password, go to your Teltonika device web UI and select Services -> SMS Gateway -> Post/Get Configuration. Check "Enable" and set your username and password. These are not the same credentials as you use for web UI. 

### Contributing
If you'd like to contribute by reporting a bug or feature request, open an issue. Pull requests are also welcome. 
If you succesfully use it with devices other than listed above, please let us know!

For more details visit Teltonika docs:
https://wiki.teltonika-networks.com/view/RUT240_SMS_Gateway

