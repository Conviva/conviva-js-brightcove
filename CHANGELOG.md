
# Changelog

## 4.0.9 (25/SEP/2020)
* Introduces new event listener to handle 'dispose' event for stopping conviva monitoring.
* Fixes auto detection of the isLive for Live contents. 

## 4.0.8 (08/SEP/2020)
* Supports Brightcove Player 6.44.
* Fixes the issue of isLive and bitrate not reported for the replay content.
* Introduces handling of events 'contenterror' and 'aderror' which gets thrown when main content fails to load in exceptional cases as per feedback from Brightcove team.

## 4.0.7 (13/JUL/2020)
* Fixes the under reporting of the Video Startup Failures metrics by changed the order of the event listeners: Registering all the events on 'ready' callback and ensuring all the event listeners are active during Conviva monitoring.
* Optimises the logic of extracting mediainfo from playlist and player objects.


## 4.0.6 (29/MAY/2020)
* Supports Brightcove Player 6.42.
* Uses an upgraded version of SDK architecture (4.0.10 and above) that simplifies and accelerates Conviva integration using Analytics and VideoAnalytics classes.
