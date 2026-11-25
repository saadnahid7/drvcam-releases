# Changelog

All notable user-facing changes to DRVCAM. Each entry matches a signed release on this
page; verify any download against its `SHA256SUMS.txt` before installing. One APK covers
Android 9–17 (phone = arm64, emulator = x86_64). Product page and docs:
**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**.

Signing certificate SHA-256 (all releases): `d705c053bd41b95af6d10f00ac69ce5daf4f7320778e0965d139fb7377e05869`.
Builds modified or re-signed by anyone else are unsupported and receive no licences; always
update older builds to the latest.

> Earlier 0.9.4–0.9.7 alpha builds were published during early testing and are kept as
> drafts for their download history; they are superseded by the releases below.

## 1.0.7 (versionCode 91)

Stable release over 1.0.6.1.

### New
- Larger video sources — the import size limit has been removed. Import full-length
  videos, bounded only by your free storage.

### Improved
- Faster, lighter setup — enabling a source into a camera app is quicker and uses less
  storage, with no duplicate per-app copy of your media.
- The source stays available after a reboot without re-enabling it.

## 1.0.6.1 (versionCode 90)

Minor bug fixes over 1.0.6.

### Fixed
- Minor bug fixes and stability improvements.

## 1.0.6 (versionCode 89)

Hotfix over 1.0.5.

### Fixed
- The app could get stuck on, or close at, the splash screen on some devices — most often
  after upgrading from an older version. It now recovers to a Retry / sign-in screen instead
  of hanging, so you can always get back in.
- Some phones signed you out, or sat on "checking", after a restart — most often on rooted
  devices running a secure-keystore spoofing module, where the keystore is briefly unavailable
  right after boot. The app now stays signed in across the reboot and recovers on its own once
  the keystore is ready, instead of locking you out until you sign in again.

## 1.0.5 — first stable (versionCode 88)

### New
- First **stable** DRVCAM release.
- Android 12L (API 32) is now a qualified version for camera replacement.

### Fixed
- Sign-in failed on some phones whose secure keystore could create a key but not sign with
  it (seen on certain custom-ROM / GSI devices): the app now signs in on these devices.
- Sign-in could fail on some devices with vendor-specific secure-key providers.
- The photo source could fail to load inside camera apps with a small memory budget; it is
  now scaled to fit and loads reliably.
- The free-mode screen now explains the actual reason a free start failed instead of a
  generic "not available" message.

## 1.0.4-beta (versionCode 87)

### New
- TikTok LIVE: the audio from your selected video now plays during a live broadcast, not
  only in recorded videos.
- Russian is now available as an app language.

### Fixed
- The app could get stuck on the splash screen after a failed start-up check; it now
  recovers to the sign-in screen instead of hanging.
- Taking a photo failed in some camera apps on Android 9–12; still photos now capture
  correctly.
- Injected video audio could drop out in some apps (for example Snapchat), and switching
  the microphone source could need two taps; both are fixed.

## 1.0.2-beta (versionCode 85)

### New
- Resolution picker on the live screen (Auto, 1080p, 1440p, 4K) for a sharper picture in
  apps that capture at a lower size.
- Starting the free trial now asks for a valid email address.

### Fixed
- TikTok could crash on launch while DRVCAM was active; TikTok now opens normally and
  recorded-video audio can be replaced.
- Some phones signed you out after every restart and showed "This device could not be
  registered"; you now stay signed in.
- Samsung Galaxy S24 and other phones with vendor-specific camera streams could show a
  black screen; these camera sessions now work.
- Enabling an app failed on Vector-SR with a "No value for API Version" error; it now works.
- Enabling an app could fail with "Operation incomplete (exit 137)", or stop halfway on
  phones where the system blocks the app-stop command, leaving a black camera.
- An app could close on phones with low graphics memory while the camera was active; the
  frame is now skipped instead and the camera keeps running.

## 1.0.1-beta (versionCode 75)

### New
- Photo capture mode: take still photos through your virtual camera, not just video.
- Live network stream: use an RTSP/RTMP stream as your camera source.
- Remote Diagnosis: support can connect remotely to help fix issues on your device.
- Search and refresh in the app picker, so finding and adding apps is easier.
- Plan info and support links added to the sign-in and upgrade screens.

## 0.9.8-alpha (versionCode 63)

### New
- A single build for Android 9–17 (previously separate 9–11 and 12–17 builds). Checked on
  an Android 9 emulator and on Android 16 with a phone.
- Optional audio source (Settings → Preferences), the Messenger video-call picture fix, and
  the floating-controller hint when an app is not hooked yet (carried from 0.9.7).
