# Axis A8105-E door station with video

Tested working with CUCM 12.5 with video calling to Jabber 12.9 and 9971 series endpoints

The biggest issue was that the device did not assume to send the call to the registrar server. The `To SIP address:` needed to include the CUCM server DNS/IP. Shoutout to Axis support for the three hour call to help figure this out.

## CUCM configuration

Build a Phone security profile to allow for digest authentication

**System -> Security -> Phone Security Profile**

Add New, pick `Third-party SIP Device (Advanced)`

Add a useful name for the `Name*` example *Axis SIP Device Security Profile*

<image here>