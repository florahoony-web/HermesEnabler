# Build & Install Notes (personal copy)

Build HermesEnabler2 and install it on your own Apple Watch, signed with your own Apple ID.

## Requirements
- A Mac with **full Xcode 26+** (App Store, ~10 GB; Command Line Tools alone won't open the project).
- Your iPhone with the Apple Watch paired.
- watchOS must be **27.0 through 27.3 beta 1** (Watch: Settings → General → About). Outside that range the app refuses to write.
- A paid Apple Developer account ($99/yr) is recommended — a free personal signing profile strips the App Group entitlement the sandbox escape needs.

## Steps
1. Clone your copy:
   `git clone https://github.com/florahoony-web/HermesEnabler.git`
2. Open `HermesEnabler2.xcodeproj` in Xcode 26.
3. In Signing & Capabilities, set the Team to your Apple ID / developer team.
4. Connect iPhone (watch paired), select your Apple Watch as the run destination.
5. Click **Run**. It builds and installs to the watch.
6. Open HermesEnabler2 on the watch, create the initial backup, then toggle the faces you want and restart Carousel when prompted.

## Safety
- It modifies the watch's MobileGestalt DeviceBrand value. Reversible via the app's backup/restore; a watchOS update may wipe it.
- Use at your own risk (MIT licensed, from pookjw/HermesEnabler).
