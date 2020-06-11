---
title: Motion controller FAQs
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Motion controllers
---


# Motion controller FAQs

## My Motion controllers aren't working properly.

If your [motion controllers](https://support.microsoft.com/en-us/help/4040517/windows-10-controllers-windows-mixed-reality) aren’t working, aren't connecting, or if you don’t see an image of the controllers when you’re wearing your headset, try the following:
1. Make sure your controllers are turned on. To turn them on, press and hold the Windows button for two seconds.
2. Make sure the controllers are fully charged and replace the batteries if they are not.
3. Turn the controllers off and on again while holding them in front of you. Press and hold the Windows button for four seconds to turn a controller off, then press and hold it again for two seconds to turn it on. 
4. Select **Settings > Devices > Bluetooth & other devices** on your PC and make sure the controllers are listed as paired. If they’re not, you’ll need to [pair them](https://support.microsoft.com/en-us/help/4040517/windows-10-controllers-windows-mixed-reality). 
5. Make sure the motion controllers show up as "Connected". "Paired" does not necessarily mean the controllers are connected to the PC. Controllers should appear under "Mouse, keyboard & pen" category. Motion controllers under "Other devices" have failed the pairing process and are not functional. Check the motion controllers LEDs: Brightly lit controllers are paired and connected, dimly lit controllers aren't connected.
6. Go to **Start  > Mixed Reality Portal** on your PC and select "Menu". You should see your motion controllers listed, along with a status message:
    * Ready – The controllers are all set.
    * Lost tracking – Mixed Reality Portal can’t find your controllers. Hold them in front of your headset and restart them by pressing the Windows button for 4 seconds, then again for two seconds.
    * Low battery – Replace the controller batteries.
7. If you're using an external USB Bluetooth Adapter, make sure it’s plugged into a black USB 2.0 port. It should also be plugged in as far away as possible from any other wireless transmitters or USB flash drives, including the USB connector for your headset. 
8. Verify that there’s only one Bluetooth radio in the PC in the Device Manager by expanding the Bluetooth section and look for one adapter. If you are using the desktop PC configuration with built-in radio, check if an external antenna is connected. If there is no external antenna connected, it can cause tracking issues. Or use an external bluetooth dongle (USB), disable the internal Bluetooth capability, and retry pairing and connecting.
9. If the Bluetooth settings window is open in the background, many extra calls are made to the Bluetooth protocol. Close it.
10. Check the virtual battery level on the motion controller by turning the controllers over in mixed reality to see the battery icon. Replace the batteries if the icon is red. Battery reporting typically reports higher than the actual level immediately after connecting a controller so wait about 15 seconds before reading the level.
11. Remove Bluetooth headphones and speakers in **Settings > Devices > Bluetooth & other devices**, and turn the devices off. Use the headphone jack or built-in speakers on your Mixed Reality headset for the best audio experience.
12. Remove other Bluetooth devices that may be paired with your PC, such as headphones or gamepads. Go to **Settings > Devices > Bluetooth & other devices on your PC**, select the devices, and then "Remove device".
13. Unplug the USB cable on your headset and plug it back into the PC to restart the controller functionality on the PC.
14. Controller lights flash when they are undergoing a firmware update. Wait for the firmware update to complete and the controllers should appear in Mixed Reality.
15. Make sure your PC is connected to a 5GHz Wi-Fi network. If your laptop is connected to a 2.4GHz Wifi network, it is typically sharing the Bluetooth connection. This may negatively impact either Wifi or Bluetooth performance, depending on the product design. Change the preferred band to 5Ghz in the network adapter settings. If your network does not support 5GHz, a Bluetooth dongle can be used instead of the internal Bluetooth capability.
16. If your Bluetooth settings have motion controllers already paired, Windows won’t discover the new devices until those are removed (if they have been added using a specific dongle, they can be only removed with that dongle).
17. If your PC has built-in Bluetooth and you’re having connection problems, try using a USB Bluetooth adapter instead. To do this, you’ll need to turn off your built-in Bluetooth radio in Device Manager and then pair your other Bluetooth devices with the new adapter.

## Motion controller troubleshooting flowchart

![Troubleshooting Flow Chart for Motion Controllers](images/motion-controllers.jpg)

## My controller is stuck in an infinite reboot (buzzing after LEDs cycle).

This is a critical battery indicator, so make sure you have fresh batteries in the device. If the issue persists, [reset the controller to factory settings](motion-controller-problems.md#how-can-i-restore-the-controllers-to-factory-settings).

## I'm trying to pair my controllers, but they never show up in the "Add a new device menu" in Bluetooth Settings.

Check that you do not have controllers paired already, remove them, and try again. If problem persists restart the PC and try again. If that fails, see more [information about Bluetooth](motion-controller-problems.md#how-can-i-tell-if-im-using-bluetooth-technology) section.

## Wi-Fi speeds becomes slow on my notebook when motion controllers are turned on.

Your notebook may share its Wi-Fi antenna with Bluetooth when connected to a 2.4GHz access point. Check from device manager if you can switch band preference to 5GHz. If a 5GHz network is not available and performance is severely impacted, consider using a Bluetooth dongle.

![Wifi band selection settings can be found through device manager](images/wifi5ghz.png)

## My second controller takes a long time to reconnect.

Some older Intel radios experience this issue if motion controllers are powered on at the same time. Avoid powering on controllers at the same time.

## My Qualcomm Bluetooth radio cannot pair controllers after a PC crash.

Qualcomm (QCA) Bluetooth radio drivers prior to 10.0.0.448 may end up in bad state after a Windows crash. Power off the PC completely to workaround this problem. 

## I'm experiencing poor controller tracking with Marvell radio.

Go to **Device Manager > Bluetooth > Marvell AVASTAR Bluetooth Radio Adapter > Properties > Driver** and make sure that you are using driver 15.68.9210.47 or later.

## The Mixed Reality Portal is working, but my controllers are tracking poorly (flying away, shaking, etc.).

1. Some lighting conditions can affect tracking. Make sure that you are not exposed to direct sunlight and that you don't have a lot of point light sources visible to your HMD (for example, strings of lights like a christmas tree). 
2. These symptoms are generally caused by failures to communicate between the controller and the host PC, and indicate poor Bluetooth link quality. See the [questions about Bluetooth](motion-controller-problems.md#how-can-i-tell-if-im-using-bluetooth-technology).

## Motion Controller LEDs are not lit, but the buttons and thumbstick still work in Mixed Reality Portal.

The Motion Controller calibration cache may be corrupt. To delete the cache, run the following command in an Administrator Command Prompt:

`rmdir /S /Q C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\Windows\MotionController\Calibration`

This folder is not accessible in Windows Explorer and can only be modified from an Administrator Command Prompt. After you have deleted the folder, restart your PC and reconnect your Motion Controllers to restore the calibration files.

## Motion controllers do not appear in SteamVR apps and games.

If you're able to see your motion controllers in the Cliff House, but not in SteamVR apps and games, the motion controller model driver may not be installed properly. This driver is automatically downloaded and installed via Windows Update, but if you're on a PC that has enterprise policies or if Windows Update is otherwise restricted, you may need to install this manually. To check that the motion controller model driver is correctly installed:
1. Turn on both of your motion controllers. Go to **Settings > Devices > Bluetooth & other devices** and make sure they show up as "Connected". If they do not show up or show up as "Paired", [pair them](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/set-up-windows-mixed-reality).
2. Go to **Device Manager > Bluetooth** and look for "Motion controller - Left" and "Motion controller - Right".
3. Select either device and then go to **View > Devices by Connection**.
4. You will now see a view of the motion controller Bluetooth devices roll up to your Bluetooth radio. Under the same node as the two Motion Controllers should be two "Bluetooth HID Device" devices, and under each Bluetooth HID Device should be devices named "Motion Controller" (with gray icons).
5. Double click each of the "Motion Controller" devices and go to the "Driver" tab. Confirm that the Driver Version listed corresponds to one of [these Motion Controller model driver versions](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/mixed-reality-software#mixed-reality-motion-controller-model-driver-release-history).

To manually download and install the Motion Controller model driver, visit [this page](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/mixed-reality-software#mixed-reality-motion-controller-model-driver-release-history) and look for the driver version corresponding to your version of Windows 10. Installation instructions are available on the download page.

## The controller firmware update takes significantly longer than two minutes.

Check the [Bluetooth questions section](motion-controller-problems.md#how-can-i-tell-if-im-using-bluetooth-technology). Poor Bluetooth link quality usually causes these problems.

## I just inserted fresh batteries but the controller virtual battery level does not indicate full level.

Motion controller battery level is tuned for AA batteries. Some low voltage rechargeable batteries may not report as full although being fully charged.

### My controller does not vibrate.

Replace your batteries. Haptics are disabled when the battery level gets low.

## My device vibrated three times and then shutdown.

Replace your batteries (they are running low and hit the cut-off threshold). 

## My Samsung motion controller’s touchpad is off-center or has a dead spot.

This is probably a hardware defect and you should go back to your retailer or equipment manufacturer for a replacement or exchange.

## How can I restore the controllers to factory settings?

Restore it to factory conditions (you'll need fresh batteries):
1. Unplug and power off the controllers.
2. Open the battery cover.
3. Insert your new batteries.
4. Press and hold the pairing button (the tab at the bottom under the batteries).
5. While holding the pairing button, power on the controller by pressing and holding the Windows button for five seconds (keep both buttons depressed).
6. Release the buttons and wait for controller to power on. This takes up to 15 seconds and there are no indicators when device recovery is happening. If device powers on immediately on button release, the recovery button sequence did not get registered and you need to try again.
7. Go to **Settings > Bluetooth > other devices**, and select "Motion controller - Left" or "Motion controller - Right" and "Remove device") to remove old controller associations from Bluetooth settings. 
8. Pair the controller with the PC again.
9. After connecting with the host and headset, the device will update to the latest available firmware.

## How can I tell if I'm using Bluetooth technology?

Motion controllers use the same Bluetooth technology found in many consumer devices and are designed to work with the Bluetooth capability included in any recent PC. To verify that your PC has a Bluetooth radio (it should if the device passed the Mixed Reality Compatibility Checker): 
* Right click on the Windows Start Menu and select "Device Manager". 
* Expand the Bluetooth section and look for an adapter. 

![Screenshot of an Example Device Manager. The Adapter is the Bluetooth radio.](images/devicemanagerbtadapterpic.png) 

If your PC doesn’t have Bluetooth, one recommended dongle is the [Plugable USB Bluetooth 4.0 Low Energy Micro Adapter](https://www.amazon.com/Plugable-Bluetooth-Adapter-Raspberry-Compatible/dp/B009ZIILLI/ref=sr-1-1?ie=UTF8&qid=1490148230&sr=8-1&keywords=plugable+broadcom).

## My PC has Bluetooth technology but I'm having problems with my controllers.

Motion controllers should work with other Bluetooth keyboards, mice, and game controllers, but the experience will vary depending on the model of keyboard, mouse, or game controller you use. Here are some things you can do to improve performance:
* If your computer has Bluetooth but you are still having problems with the motion controllers, consider replacing your Bluetooth radio with the Plugable external Bluetooth Adapter plugged into USB. Note that you can only have one Bluetooth radio adapter active at a time. If you plug in an external radio in addition to an existing radio you need to disable your existing Bluetooth radio in Device Manager (right-click on the adapter and select "Disable Device") and un-pair/re-pair all of your previous Bluetooth devices.
* If you're using a USB Bluetooth Adapter, connect it to a USB 2.0 port (2.0 ports are black and aren’t labeled "SS"), if available. The port should be physically separated from:
    - the HMD USB connector
    - flash drives
    - hard drives
    - wireless USB receivers like those for keyboards/mice
Ideally, plug the USB Bluetooth Adapter into the opposite side of the computer as far as possible from these other connectors.
* Do not install any third-party software.
* Close the Bluetooth settings window if it's open. Leaving it open in the background means that a lot of extra calls are made to the Bluetooth protocol.
* Disable "Show notification to connect using Swift Pair" setting under Bluetooth & other devices to reduce host radio scanning activity.
* If you are using an internal Bluetooth card, please ensure you are using an external Bluetooth antenna or you may experience tracking issues. If this doesn’t work, use an external Bluetooth dongle (USB) after disabling the internal Bluetooth.
* It is important that the device appears under the "Mouse, Keyboard & Pen" category in the Bluetooth settings. If under "Other devices" then unpair and pair the device.
* Remove, unpair, and power off Bluetooth headphones and speakers. These are not supported with Windows Mixed Reality. You can use the headphone jack or built-in speakers on your Mixed Reality headset for the best audio experience.

## Should I pair my controllers to a Windows Mixed Reality headset that has built-in Bluetooth radio?

Some Windows Mixed Reality headsets, including the Acer OJO 500 and Samsung Odyssey+, have built-in Bluetooth radios for use with motion controllers. The motion controllers that come with these headsets are pre-paired to the headset from the factory, and do not require your PC to have a separate Bluetooth radio. These motion controllers _can_ be manually paired to your PC's Bluetooth radio, for example, for use with Windows Mixed Reality headsets that do not have built-in Bluetooth radios. 

## How can I return my controllers to their factory pairing?

To return the motion controllers to their factory pairing, or to pair them with a Windows Mixed Reality headset with built-in Bluetooth radio, run the headset's device companion app (for example, the "Acer OJO 500" app or the "Samsung HMD Odyssey+ Setup" app, automatically installed the first time the headset is plugged in) and follow the instructions for motion controller pairing.

## Lights and indicators

The LED constellation ring and haptics indicate the state of the motion controller.

| State    | What causes the state | Light and vibration behavior associated with the state |
|----------------------------|-----------------------------|----------------------------------------------------------------------|
| **Power on**               | Press and hold Windows button on controller for two seconds to turn on the controller.       | LEDs turn on and controller vibrates once. |
| **Power off**              | Press and hold Windows button on controller for four seconds to turn off controller.      | LEDs turn off and controller vibrates twice. |
| **Sleeping**               | The controller enters sleeping state automatically when it’s motionless for 30 seconds. The controller automatically wakes when it detects motion except when the device is not paired with the host PC. In that case, a button press will be required to wake it up. | LEDs turn off and blink every three seconds while in sleeping state. |
| **Pairing**                | Press and hold pairing button inside battery case for three seconds.     | LEDs slowly pulse while in pairing mode, and go solid when exiting pairing mode. The controller vibrates once if pairing was successful or vibrates three times if pairing is unsuccessful and times out. |
| **Controller connects/disconnects from PC** | The controller successfully connects to PC after you turn it on, or the controller disconnects from the PC during use for some reason.| The controller vibrates once on PC connection or disconnection. |
| **Low Battery Level**      | The battery level is low.| There is no LED or vibration indication when battery is low. There is a battery indicator icon on the handle of the controller representation in headset. When battery is low, the indicator icon will show 1/4 full. |
| **Critical Battery Level** | During power on when battery level is "Critical". "Critical" battery level means there is insufficient power and the controller will turn off automatically.| The controller vibrates three times when you turn it on and then automatically turns off. As you approach this state, the battery indicator icon will display red. |
