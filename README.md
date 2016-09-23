# HDHRViewerV2.bundle
Watch Live TV on Plex using HDHomeRun, at home or remotely. Compatibility may vary by Plex Media Server (PMS) version, Plex client version, etc... 

## Installation
### Method 1 : Unsupported AppStore V2 (UAS V2)
Available through UAS V2 <https://forums.plex.tv/discussion/202282/unsupported-appstore-v2-as-in-totally-unsupported>

### Method 2 : Manual Installation
Copy HDHRViewerV2.bundle to Plex Plug-in Directory. [How do I find the Plug-Ins folder?](https://support.plex.tv/hc/en-us/articles/201106098-How-do-I-find-the-Plug-Ins-folder-)

### Method 3 : Scripts
Run install scripts included.

## HDHomeRun Compatibility

Compatible with HDHomeRun that have DLNA or HTTP streaming capabilities.

### Compatible
- HDHomeRun PRIME (HDHR3-CC)
- HDHomeRun 4DC (HDHR3-4DC)
- HDHomeRun DUAL (Gen4)
- HDHomeRun CONNECT (HDHR4-2US/2DT)
- HDHomeRun PLUS/EXTEND (HDTC-2US)
- HDHomeRun EXTEND (HDTC-2US-M)

### Not Compatible
- HDHomeRun DUAL (HDHR3-US/EU/DT)
- HDHomeRun DUAL (HDHR2-US/DT)
- HDHomeRun DUAL (HDHR-US/EU/DT)

Please use [HDSurfer Plug-in for HDHomeRun](https://forums.plex.tv/discussion/83233/hdsurfer-plug-in-for-hdhomerun)

## Server Compatibility/Requirement

Standard Plex requirement for streaming to Plex Home Theater (PHT)

High CPU requirement for transcoding to other clients (Web/Android/Roku/FireTV/etc…). Typical NAS devices may not have capable CPU for transcoding.

Estimated CPU requirement for 1080i MPEGTS transcoding:
- Intel Core2 Quad 2.5Ghz or faster.
- Intel Celeron/Pentium Gxxxx 3Ghz or faster.
- Intel i3/i5/i7 Dual Core (1st Generation) 3Ghz of faster.
- Intel i3/i5/i7 Dual Core (Later Generation) Turbo Speed 2.5Ghz or faster.
- AMD Athlon Quad Core 3Ghz or faster.
- AMD AthlonII/Phenom/A6/A8/A10 Quad Core 2.5Ghz or faster.

## Client Compatibility

Some browser may have playback issues with HTML5 player, disable HTML5 player. Refer to Known Anomalies for more info.

Refer to <https://github.com/zynine-/HDHRViewerV2.bundle/wiki/Server-Client-Compatibility-Report>

## Known Anomalies

###Interlacing

There is no known method of forcing deinterlacing support from plug-in level. Deinterlacing is achieved by replacing xml profiles, <https://github.com/zynine-/PlexDeinterlaceProfiles>.

###Slow buffer or stutters on some clients

On some clients, setting a lower stream quality may increase loading, or stutters. This is due to the video chunk size; PMS seem to love 4MB chunk sizes.

Ways to reduce loading times or stutters:
- Disable HTML5 if you are using a browser
- Set higher quality, or the highest your network bandwidth/connection allows.

###Android support
Since PMS 0.9.17.x, Android devices without AC3 codec have playback issues. You can use *VLC for Android* as *External Player*, but it doesn't transcode the stream. Instead, use the Android.xml from <https://github.com/zynine-/PlexDeinterlaceProfiles>
