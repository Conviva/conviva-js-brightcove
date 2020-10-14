
# Changelog

## 4.1.0 (14/OCT/2020)
* Introduces a major change to the conviva monitoring logic based on Brightcove and Video.js player events especially 'play', 'playing', 'ended' and 'abort'.
* Introduces auto detection of new custom tag "has_ads_started" to signify the start of ad playback.
* Fixes reporting of extra playing state during low bandwidth scenarios for Live contents.
* Fixes Conviva monitoring when the Skippable Linear ads are failing by relying on 'adserror' event to resume monitoring.
* Fixes intermittent non reporting of PLAYING/BUFFERING player states upon end of midroll ad playback.
* Fixes non reporting of "has_ads_error" for the VMAP Ad failures by relying on 'ima3-log' event.

## 4.0.9 (25/SEP/2020)
* Introduces new event listener to handle 'dispose' event for stopping conviva monitoring.
* Fixes auto detection of the isLive for Live contents. 

## 4.0.8 (08/SEP/2020)
* Supports Brightcove Player 6.44.
* Introduces handling of events 'contenterror' and 'aderror' which gets thrown when main content fails to load in exceptional cases as per feedback from Brightcove team.
* Introduces auto detection of new custom tags "has_ads_requested", "has_pod_started" and "has_ads_error" to signify the ad playback events.
* Fixes the issue of isLive and bitrate not reported for the replay content.

## 4.0.7 (13/JUL/2020)
* Fixes the under reporting of the Video Startup Failures metrics by changed the order of the event listeners: Registering all the events on 'ready' callback and ensuring all the event listeners are active during Conviva monitoring.
* Optimises the logic of extracting mediainfo from playlist and player objects.


## 4.0.6 (29/MAY/2020)
* Supports Brightcove Player 6.42.
* Uses an upgraded version of SDK architecture (4.0.10 and above) that simplifies and accelerates Conviva integration using Analytics and VideoAnalytics classes.
