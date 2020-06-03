---
title: Speech and audio problems
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Audio problems, Speech problems
---


# Speech and audio problems

## I can't hear any sound in my headset, or sound is playing through my computer instead of my headset.

* If your immersive headset doesn’t include built-in headphones, you’ll need to connect headphones to the audio jack on the headset. The jack is often located just behind or under the headset visor or lenses. Check with your headset manufacturer if you can't find it.
* Some audio headsets have physical buttons to control the volume. If audio isn't working, check to see whether the volume is turned down or muted.
* Windows Mixed Reality is designed to play sound through your immersive headset when the Mixed Reality Portal is running and you have headphones connected to it. When you take the headset off or flip the visor up, close the Mixed Reality Portal application, or when that app has not been used for 15 minutes, audio will switch to your default Windows playback device. You can change this setting in **Settings > Mixed reality > Audio and speech.**
* Make sure your audio headset is plugged into the audio jack completely. The Acer headset in particular may require more care to ensure the audio headset is plugged in all the way.
* Check that the audio headset/microphone is plugged into the headset and not the PC.
* The Windows Sound Control Panel only shows enabled audio endpoints, not disabled endpoints. The headset audio device will be disabled when you're not wearing the headset, so you have to right-click in the sound control panel and choose "Show disabled devices" to see it; the device name is "Realtek USB2.0 Audio". Once you do this, you can change the name in the "Properties" page to something you'll recognize more easily. You can do this for both the playback and recording tabs.
* If your audio is not working in Mixed Reality apps (for example, Netflix), this may be caused by a known issue where Windows Mixed Reality is not be automatically updated to match the OS version. To fix this issue and get the best Mixed Reality experience, go to **Settings > Update & Security > Windows Update > Check for Updates**.

**Note:** Windows Mixed Reality spatial audio works best with headphones built into or connected directly to your immersive headset. PC speakers or headphones connected to the PC might not work well for spatial audio.

**Note:** Windows Mixed Reality doesn’t support Bluetooth audio headsets.

## I'm experiencing sudden volume changes, lost audio, or buzzing.

* Some applications, including many of those launched through SteamVR, can lose audio or hang when the audio device changes as you start or stop the Mixed Reality Portal. Restart the app after you have opened the Mixed Reality Portal app to correct this.
* If another multimedia USB device (such as a web cam) shares the same internal or external USB hub with the Windows Mixed Reality headset, the headset's audio jack/headphones may occasionally have a buzzing sound or no audio at all. Plug your headset into a USB port that uses a different hub or disconnect/disable your other USB multimedia device.
* If you notice a loud burst of noise from headphones connected to the headset, it is possible that the PC's USB hub is not able to provide enough power to the Windows Mixed Reality headset. If this occurs, file a [Feedback Hub](https://docs.microsoft.com/hololens/hololens-feedback) bug immediately. Workarounds that may help include not using extension cables, using a dedicated, external powered USB 3.0 HUB, or trying a different USB port on the PC.

## My Bluetooth audio headset isn't working as expected.

Microsoft does not recommend using Bluetooth audio headsets with Windows Mixed Reality. Bluetooth audio peripherals do not work well with Windows Mixed Reality voice and spatial sound experiences, and Bluetooth audio headsets cannot support microphone input and stereo output at the same time, so you won't hear stereo or spatialized sound when using it for gamechat or other voice input. Bluetooth audio headsets can also negatively affect your motion controller experience. 

## Sound isn't coming from expected directions.

The Windows Mixed Reality home includes spatial sound (audio that sounds like it comes from the apps located in your home). As you turn around and move closer or farther from each app, the sound direction and level will change to further the sense of realism. Here are some reasons for unexpected sound directions: 
* When you open and play music from a background-capable music app (like Groove Music) in your home and then open an immersive VR experience (like a game), the sound from the music app will crossfade from spatial sound to stereo. It may appear louder than before because there is no longer any distance between you and the sound.
* If you had Cortana enabled on your host PC prior to using your Windows Mixed Reality headset, you may lose the spatial sound applied to the apps in your Windows Mixed Reality home. To fix this, either turn off "Let Cortana respond to Hey Cortana" in **Settings > Cortana** on your desktop before launching Windows Mixed Reality, or enable "Windows Sonic for Headphones" from within the Desktop app window in Windows Mixed Reality home:
    1. Left-click the speaker icon on the desktop taskbar and select it from the list of audio devices.
    2. Right-click the speaker icon on the desktop taskbar and select "Windows Sonic for Headphones" in the "Speaker setup" menu.
    3. Repeat these steps for all of your audio devices (endpoints).

## Speech commands are not working as expected.

* To use speech commands, speech and language settings on your PC must be set to a [language supported in Windows Mixed Reality](https://support.microsoft.com/en-us/help/4039262/windows-10-mixed-reality-setup-faq#Languages). To check your Windows speech and language settings, select **Settings  > Time & language > Region & language** and **Settings  > Time & language > Speech**.
* If your headset doesn’t have a built-in microphone, you’ll need to attach headphones with a microphone to the headset or to your PC. To have microphone input switch automatically to your headset when you wear it, go to **Settings > Mixed reality > Audio and speech**, and turn on "When I wear my headset, switch to headset mic".
* Some audio headsets have a physical button to mute and unmute the microphone. If speech commands aren't working, check to see whether your microphone is muted.
* Audio headsets with a microphone that dangles from the earbud cable do not perform well for voice commands in environments with ambient noise.
* Cortana can be slow the first time she is invoked in a Mixed Reality Portal session. Go to **Settings > Cortana > Talk to Cortana** and make sure "Let Cortana respond to Hey Cortana" is enabled.
* On some PCs, the default voice capture gain for your headset-connected microphone may be set too low. If you experience unreliable speech commands or dictation, you can try running the Microphone Setup troubleshooter. You can reach this troubleshooter through the **Settings > Time & Language > Speech**, then select "Get Started" in the "Microphone" section. Do this through the Desktop app in the Windows Mixed Reality home while wearing the headset to affect the microphone you use for Windows Mixed Reality. Select the appropriate endpoint in the troubleshooter wizard.

## I only have one audio headset and I want to use it for both Desktop and my headset.

If you only have one audio headset and do not have a headset with built in headphones, connect the audio headset to the host PC instead of the headset. Then turn off "switch to headset audio" in the MRP settings.

## I want to switch to Dolby Atmos for Headphones.

Windows Mixed Reality environments and its applications use Windows Sonic for Headphones spatial audio technology which is customized for mixed reality experiences. Other spatial audio technologies, like Dolby Atmos for Headphones, can be applied for full screen applications like SteamVR games but not for the Windows Mixed Reality shell environments and applications (such as placing a web browser on the wall of the Cliff House or the Sky Loft) which have been designed using Windows Sonic for Headphones spatial sound and acoustics.