
# Dell m3800 OpenCore

Fork from https://github.com/adrgumula/oc-m3800  All credits to adrgumula.

OC 0.7 with fan control customization. Tested on macos Big Sur 11.4.

Works and tested:
+ 3D accelelation (2GB vram + framebuffer patched: 160MB bios, 48MB),
+ Wifi (I replaced the original M3800 wifi module with the compatible one),
+ Blutooth (patched),
+ HDMI/DVI video
+ HDMI audio
+ Keyboard
+ Battery
+ Multimedia keys (volume, screen brightness)
+ night shift
+ camera
+ disabled Nvidia
+ 4k/60Hz internal screen - BigSur / no screen flickering
+ light sensor
+ Touchpad with guestures
+ iMessage, FaceTime


Not/partially working
- sleep & wake on battery and AC power (sleeps ok but black screen after wake up)
- Lid close sleep & wakesup after Lid open (sleeps ok but black screen after wake up)
- Touchable screen (no response)


Customize fan control:
1. Done through I8k.kext
2. Modify its Info.plist for fan control custimization.
##
    <key>I8kTemperatureFanHigh</key>
    <integer>55</integer>
    <key>I8kTemperatureFanIdle</key>
    <integer>40</integer>
    <key>I8kTemperatureFanLow</key>
    <integer>45</integer>
