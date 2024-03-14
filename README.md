# Arduino Watchdog for Routers
This is at the moment just a scratch pad for a little project I aim to build.

Problem: I have a Linksys LRT-224 and Linksys LRT-214 that handles all my inbound and outbound traffic for my home LAN where I run some web-scrapers and other types of services. I don't want it to loose connectivity as these services might go down or require manual restarts, it also affects the Wifi and then it becomes my "fault" that "internet is broken".

Solution: A simple Arduino-clone (Wemos D1) is used to monitor the routers status through:
* SNMP
  * Get WAN-side IP address
  * Get Uptime ticks
* HTTP
  * Get administrative pages
  * Get external API's
 
If any/both routers (or the arduino itself) would detect a fault-state, this would trigger a NC (Normally Closed) relay to go OPEN, breaking the circuit for a short while and then go back to NC to restart the device.


Linksys LRT-224 + Linksys LRT-214
* 12v


Arduino Wemod D1
* 5v


## BOM - Bill of material


## SBOM - Software bill of material
