
# Changelog

## 4.2.2 (27/APR/2021)
* Supports Brightcove Player 6.51.2 version
* Enhances the support for the application to provide accurate information for the following metadata from Brightcove Studio:
  * duration: auto detects based on the value available in mediainfo set while uploading media or player.duration()
  * isLive: auto detects based on the value available in custom_fields "isLive" or mediainfo set while uploading media or options "isLive" or player.duration()
  * defaultReportingResource: auto detects based on the availability of field "defaultReportingResource" in custom_fields or options
  * encodedFramerate: auto detects based on the availability of field "encodedFramerate" in custom_fields or options
  * Refer to https://conviva.developerprogram.org/site/one-sensor/sensors/web_brightcove/index_one_sensor.gsp#common-tags for more details
* Enhances bitrate reporting logic to report current playing segment bitrate instead of downloading segment for non Safari Browsers
* Enhances the “has_ads_error” custom tag auto detection by registering for adtimeout and handling ima3-log error events in all scenarios
* Introduces auto detection of new custom tags href pulled from window.location.href to identify the hostname of playback initiated
* Introduces auto collection of Screen Resolution of the display (Core SDK 4.0.18 and above)
* Introduces auto collection of Dropped Frames during playback (Core SDK 4.0.18 and above)
* Fixes the issue of inflated Play Attempts, VSF and EBVS by modifying the logic of Conviva monitoring to start on play, playing, loadstart, error events and end on loadstart, ended, abort, ads-all-pods-completed events

## 4.1.1 (28/DEC/2020)
* Supports the VHS 2 introduced by Brightcove in v6.45.4 and uses the player.tech.vhs API's over the deprecated player.tech.hls API's along with the backward compatibility for older versions.

## 4.1.0 (14/OCT/2020)
* Introduces a major change to the conviva monitoring logic based on Brightcove and Video.js player events especially 'play', 'playing', 'ended' and 'abort'.
* Introduces auto detection of new custom tag "has_ads_started" to signify the start of ad playback.
* Fixes reporting of extra playing state during low bandwidth scenarios for Live contents.
* Fixes Conviva monitoring when the Skippable Linear ads are failing by relying on 'adserror' event to resume monitoring.
* Fixes intermittent non reporting of PLAYING/BUFFERING player states upon end of midroll ad playback.
* Fixes non reporting of "has_ads_error" for the VMAP Ad failures by relying on 'ima3-log' event.

## 4.0.9 (28/SEP/2020)
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
