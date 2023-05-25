# Change Log

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
