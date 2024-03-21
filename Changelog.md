# Change Log

## v1.2.5 (Mar 21, 2024 UTC)
- Improved WebRTC internal logging
## v1.2.4 (Mar 7, 2024 UTC)
- Stability improvements
## v1.2.3 (Feb 1, 2024 UTC)
- Fix issues related to `isForeground`
## v1.2.2 (Dec 21, 2023)
- Remove duplicative dependency of WebRTC to allow simultaneous use of Sendbird Live and Calls SDK
## v1.2.1 (Dec 11, 2023)
- Added `LiveEventListener.onHostVideoResolutionChange` to monitor changes in video resolution.## v1.2.0 (Dec 01, 2023)
- Added support for streaming with multiple hosts
  - Now, multiple hosts can stream in a live event simultaneously.
  - `LiveEvent.hostType` has changed to `LiveEvent.type`
  - LiveEventType can have following values: `AUDIO_ONLY` and `VIDEO`, indicating the live event type for audio-only streaming and video streaming, respectively.
  - `LiveEventCreateParams.hostType` has changed to `LiveEventCreateParams.type`
  - `LiveEventQuery.hostTypes` has changed to `LiveEventQuery.types`
- Added event listeners for receiving connection
  - LiveEventListener.onDisconnect(liveEvent: LiveEvent, e: Error)
  - LiveEventListener.onReconnect(liveEvent: LiveEvent)
- The existing `onDisconnect` event is now renamed to `LiveEventListenere.onExited(liveEvent: LiveEvent, e: Error)`## v1.2.0-beta.1 (Nov 08, 2023)
- Added support for streaming with multiple hosts
  - Now, multiple hosts can stream in a live event simultaneously.
  - `LiveEvent.hostType` has changed to `LiveEvent.type`
  - LiveEventType can have following values: `AUDIO_ONLY` and `VIDEO`, indicating the live event type for audio-only streaming and video streaming, respectively.
  - `LiveEventCreateParams.hostType` has changed to `LiveEventCreateParams.type`
  - `LiveEventQuery.hostTypes` has changed to `LiveEventQuery.types`
- Added event listeners for receiving connection
  - LiveEventListener.onDisconnect(liveEvent: LiveEvent, e: Error)
  - LiveEventListener.onReconnect(liveEvent: LiveEvent)
- The existing `onDisconnect` event is now renamed to `LiveEventListenere.onExited(liveEvent: LiveEvent, e: Error)`## v1.1.2 (Sep 27, 2023)
- Added the isForeground in `SendbirdLive.init()`.
## v1.1.1 (Sep 25, 2023)
## 1.1.1 (Sep 5, 2023 UTC)
- Improved the internal logic of the `Sendbird.init()` function.
## v1.1.0 (Sep 07, 2023)
## Sendbird Live SDK is now out of beta.

## Introducing Audio Only Live Events.
You can stream live events with audio only, without having to turn the video on.
- Added `hostType` to `LiveEvent`
  - singleHost: live event in which one host can stream video and audio at a time.
  - singleHostAudioOnly: live event in which one host can stream only audio at a time.
  - When creating or retrieving a list of live events, you must specify the type of the live event by providing a `hostType` variable.
- Added `hostType` to `LiveEventCreateParams`
- Added `hostTypes` to `LiveEventListQueryParams`

## Breaking Changes
- `LiveEvent.onParticipantEnter` and `LiveEvent.onParticipantExit` have been removed due to the excessive number of events they triggered when numerous participants joined the live event.
  - Instead, use `LiveEvent.onParticipantCountChanged` to track the change of participant counts in a live event. This event will not be called every time a new participant joins the live event. Instead, it will be called periodically depending on the total number of participants joining the live event.
- Now, initializing the Live SDK will initialize Sendbird Chat SDK, using the default `InitParams` defined in the Chat SDK. If you wish to change the initialization parameters of the Chat SDK, you must call `SendbirdChat.init` again after the Live SDK initialization.
- `ConnectionQualityListener.onConnectionQualityUpdate()` is replaced with `ConnectionQualityListener.onConnectionQualityUpdated()`.## 1.0.0-beta.14 (June 5, 2023 UTC)
- Added bandwidth, resolution, availableBitrate to ConnectionMetrics for better information about the live event.

## 1.0.0-beta.13 (May 25, 2023 UTC)
- Modified internal logic of the `LiveEvent.switchCamera()`

## 1.0.0-beta.12 (May 24, 2023)
- Added interfaces to set video quality constraints. 
    - Added `MediaOptions.videoQualityConstraints`
    - Added `LiveEvent.updateVideoQualityConstraints()`
- Added interfaces to get network statistics from ongoing live events. 
    - Added `LiveEvent.setConnectionQualityListener`
    - Added `ConnectionQualityDelegate.onConnectionQualityUpdate`

## 1.0.0-beta.11 (May 9, 2023 UTC)
- Improve audio device management while watching or hosting a Live Event.

## 1.0.0-beta.10 (Apr 25, 2023 UTC)
- Removed the parameter of resumeStreaming().

## 1.0.0-beta.9 (Apr 25, 2023 UTC)
- Fix a bug that occurs when the network connection is lost.

## 1.0.0-beta.8 (Mar 24, 2023 UTC)
- Added `LiveEvent.getAllReactionCounts`
- Stability improvements.

## 1.0.0-beta.7 (Mar 8, 2023)
- Introducing reactions in Live Event. You can now react to live events in real time for better user interactions. 
    - Added `LiveEventCreateParams.reactionKeys`
    - Added `LiveEvent.increaseReactionCount`
    - Added `LiveEventListener.onReactionCountUpdated`
    
## v1.0.0-beta.6 (Jan 9, 2023 UTC)
- Add interfaces to support streaming from RTMP.

## v1.0.0-beta.5 (Dec 22, 2022 UTC)
- Add interfaces to support applying filters to camera feed using external video source.

## v1.0.0-beta.4 (Nov 22, 2022 UTC)
- Added onLiveEventInfoUpdated in LiveEventListener
- Improved stability

## v1.0.0-beta.3 (Nov 15, 2022 UTC)
- Added resumeStreaming and pauseStreaming in LiveEvent
- Updated WebRTC version to M106
- Improved stability

## v1.0.0-beta.2 (Oct 6, 2022)
- Added customItems and LiveEventUpdateParams in LiveEvent
- Added title and coverURL in LiveEvent
- Renamed LiveEventParams to LiveEventCreateParams
- Added getCachedLiveEvent in SendbirdLive
- Added resumeVideoCapturer in LiveEvent
- Added availableAudioDevices and currentAudioDevice in LiveEvent
- Added availableVideoDevices and currentVideoDevice in LiveEvent
- Fixed error

## v1.0.0-beta (Jul 15, 2022)
- Initial beta release
