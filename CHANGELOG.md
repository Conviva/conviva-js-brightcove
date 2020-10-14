
# Changelog

## 4.0.7 (13/JUL/2020)
* Fixed the under reporting of the Video Startup Failures metrics by changed the order of the event listeners: Registering all the events on 'ready' callback and ensuring all the event listeners are active during Conviva monitoring.
* Optimised the logic of extracting mediainfo from playlist and player objects.


## 4.0.6 (29/MAY/2020)
* Supports Brightcove Player 6.42.
* Uses an upgraded version of SDK architecture (4.0.10 and above) that simplifies and accelerates Conviva integration using Analytics and VideoAnalytics classes.
