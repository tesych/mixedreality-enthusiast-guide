---
title: Error codes and how to resolve them
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Error Codes
---



# Error codes and how to resolve them

| **Windows 10 error codes** (version 1809/versions 1709, 1803) | **Error message and troubleshooting suggestions**                    |
|-------------------------------------------------------------|--------------------------------------------------------------------|
|   1-4 / 2197815297-4  | **Check your display cable: Make sure your headset's display cable is plugged in correctly.** <br/><br/><ol start="1"><li>Unplug both your headset's USB and HDMI cables, then plug them back in.</li><li>Check Device Manager and confirm that under "Monitors", the "Mixed Reality headset" monitor is present.</li><li>Make sure your graphics drivers are up to date (from your graphics card manufacturer's website).</li><li>If you're using an adapter to connect your headset, make sure it [supports Windows Mixed Reality](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/recommended-adapters-for-windows-mixed-reality-capable-pcs).</li><li>If your graphics card has both DisplayPort and HDMI ports, try using the DisplayPort port on your graphics card, and use a supported Mixed Reality DisplayPort-to-HDMI adapter.</li><li>Try a different USB 3.0 port on your PC</li></ol> |
|   1-5 / 2197815297-5  | **Check your display cable: Your headset displays failed to initialize properly. Try restarting your PC and reconnecting your headset.**<br/><br/>Windows sees your headset monitor, but Windows Mixed Reality is having trouble communicating with the displays on your Mixed Reality headset. To fix this:<br/><ol start="1"><li>Make sure your graphics drivers are up to date (from your graphics card manufacturer's website).</li><li>If you're using an adapter to connect your headset, make sure it [supports Windows Mixed Reality](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/recommended-adapters-for-windows-mixed-reality-capable-pcs).</li><li>If your graphics card has both DisplayPort and HDMI ports, try using the DisplayPort port on your graphics card, and use a supported Mixed Reality DisplayPort-to-HDMI adapter.</li><li>Try restarting your PC.</li></ol> |
|   7-1, 7-2, 7-3  / 2181038087-1, 2181038087-2, 2181038087-3  | **Windows Mixed Reality is having trouble connecting to your headset. Try unplugging your headset and plugging it back in.**<br/><br/>The Mixed Reality headset failed to completely initialize. This is most likely a transient error. Unplug your headset and plug it back in to resolve this issue.
|   7-4  / 2181038087-4  | **Windows Mixed Reality is having trouble connecting to your headset. Try unplugging your headset and plugging it back in.**<br/><br/>The Mixed Reality headset driver failed to initialize the tracking cameras on your headset. This is most likely a transient error. Unplug your headset and plug it in again to resolve this issue.
|   7-5  / 2181038087-5  | **Windows Mixed Reality is having trouble connecting to your headset. Try plugging your headset into a different USB port and temporarily unplugging any other USB devices connected to your PC.**<br/><br/>Windows Mixed Reality lost synchronization between the Mixed Reality camera frame timestamps and your PC timestamps. This could be a transient error, or an indication of USB signal integrity issues. To fix this:</li><li>Temporarily unplug all of your USB devices and peripherals, remove all extension cables, and plug in just your headset.</li><li>Disable any USB suspend/power saving features on your PC, like Selective suspend in Windows power options, the "Allow the computer to turn off this device to save power" setting in Device Manager, and any USB power saving settings in your PC's firmware.</li></ul>
|   7-6  / 2181038087-6  | **There is a problem with your headset firmware. Try unplugging your headset and plugging it back in.** <br/><br/>This can be transient error. Try unplugging and re-plugging in your headset. If that doesn't work:</li><li>Check Windows Updates to ensure that you are running the latest headset driver available.</li><li>Try your headset on another PC. If you see the same error message, your headset will need to be serviced.</li></ul>
|   7-7  / 2181038087-7  | **Windows Mixed Reality is having trouble connecting to your headset. Try plugging your headset into a different USB port and temporarily unplugging any other USB devices connected to your PC.**<br/><br/>The Mixed Reality headset driver failed to initialize the firmware on your headset. This can be transient error. Try unplugging and re-plugging in your headset. If that doesn't work:<li>Temporarily unplug USB devices and peripherals you don't need to run Windows Mixed Reality.</li><li>Check Windows Updates to ensure that you are running the latest available headset driver.</li></ul>
|   7-11  / 2181038087-11 | **Your CPU is too old to be compatible with Windows Mixed Reality.**<br/><br/>Your PC is failing the compatibility check because your CPU is missing the AVX instruction set required by the Mixed Reality motion controllers. You'll need a [Windows Mixed Reality compatible PC](https://www.microsoft.com/en-us/windows/view-all-devices?col=wmr-pcs#icons).
|   7-12  / 2181038087-12 | **Your headset is connected to an incompatible USB controller. Try plugging your headset into a different USB port, if available. Or, try installing a Microsoft USB driver in place of any incompatible drivers.**<br/><br/>Your headset may be plugged in to a USB port connected to an incompatible non-Microsoft USB controller driver. These USB 3.0 controller drivers are often missing the ability to read and handle the [ContainerID descriptor](https://docs.microsoft.com/windows-hardware/drivers/usbcon/usb-containerids-in-windows), which aggregates the disparate parts of the Mixed Reality headset into a cohesive unit (to play audio out of the correct headphones, video out the correct displays, and pull tracking data from the correct sensors). To change your USB controller driver: <ol start="1"><li>Launch Device Manager.</li><li>Expand the category for Universal Serial Bus controllers and right click to uninstall the driver for each item that includes the text "eXtensible Host Controller" **and** does not have "Microsoft" in the name.</li><li>Select "Delete the driver software for this device" to ensure the old drivers are removed.</li><li>Verify that each item that includes the text "eXtensible Host Controller" has "Microsoft" at the end.</li><li>Plug in the HMD.</li></ol>Alternatively, if the issue is intermittent, the HMD might not be properly responding to commands from the HMD driver. To fix, unplug the HMD for 30 or more seconds, then plug it back in. | 
|   7-13  / 2181038087-13 | **Your headset is connected to an incompatible USB controller. Try plugging your headset into a different USB port, if available. If not, you'll need to install a new USB 3.0 controller.**<br/><br/>Windows Mixed Reality is unable to synchronize the Mixed Reality camera frame timestamps to your PC timestamps. This is most likely caused by an incompatible USB 3.0 host controller that does not support ITP (Isochronous Timestamp Packets). Contact your PC manufacturer to see if ITP can be enabled, or switch to another USB Host controller with ITP support. |
|   7-14  / 2181038087-14 | **Windows Mixed Reality is having trouble connecting to your headset. Try unplugging your headset and plugging it back in.**<br/><br/>Windows Mixed Reality is having trouble initializing the presence sensor on your Mixed Reality headset. In Device Manager, the headset will show the error message "PoseThread failed to initialize presence sensor". To fix this:<br/><ol start="1"><li>Unplug your headset, then plug it back in. Make sure the USB cable is plugged in all the way.</li><li>Try another USB port on your PC.</li><li>Try your headset on another PC to see if the headset enumerates completely in Device Manager on that PC.</li><li>Check if any other conflicting HID drivers are installed on your PC, for example from your keyboard or mouse. (Look for any HID devices in Device Manager with a question-mark logo on them.)</li><li>If you are using a Samsung Mixed Reality headset running Windows 10 Version 1709 or Version 1803, follow the instructions for error code 2181038087-12 to check if your USB 3.0 controller is running a non-Microsoft USB controller driver.</li></ol> |
|   7-15  / 2181038087-15 | **Windows Mixed Reality has detected an incompatible WinUSB driver installed.**<br/><br/><ol start="1"><li>Ensure that the WinUSB driver on your PC is the one that comes with Windows, and that any third-party USB drivers have not overwritten the copy of WinUSB on your PC.</li><li>You may need to recover or reinstall your Windows installation if the problem persists.</li></ol> |
|   13-11 / -            | The Mixed Reality Portal has encountered an app registration issue with Windows. Check the Application Event Log (using Event Viewer) to see if there are additional details. |
|   14-1  / -            | The Mixed Reality Portal is having trouble initializing the graphics and composition stack. To fix this:<ul><li>Desktop Window Manager (DWM, a key component of the Windows Graphics stack) may be crashing. Check the Application Event Log (using Event Viewer) to see if this is occurring.</li><li>Try a clean uninstall of your graphics driver, and then install the latest graphics driver from the graphics card manufacturer's website.</li></ul> |
|   14-2  / C0001160-101  | **We ran into a problem connecting to your headset. Try removing any extension cables you might be using, and make sure you've connected the headset to the correct port for your graphics card. If you're using any adapters, make sure they're compatible with Mixed Reality. If you're still having problems, try updating your graphics driver.**<br/><br/>The Mixed Reality display and composition stack failed to initialize. Your PC's graphics card or graphics card driver may not be compatible with Windows Mixed Reality. To check this: <ul><li>Double check that your PC meets the minimum system requirements for Windows Mixed Reality.</li><li>If you are using Dell Inspiron 5577 PCs on Windows 10, version 1809, or newer, you may see this error due to a conflict with Dell's TrueColor graphics post-processing functionality. To work around this issue, use Dell's TrueColor app to turn off the TrueColor capability, then try running Mixed Reality Portal again.</li><li>On a desktop PC, install the latest graphics driver from the graphics card manufacturer's website. On a laptop, install the latest graphics driver for your make and model from the laptop manufacturer's website.</li><li>If you have third party graphics or display software/accessories, temporarily uninstall these apps and drivers.</li><li>Select "Try again" to see if it's a transient issue.</li></ul> |
|   14-3  / -             | **We ran into a problem connecting to your headset. Try removing any extension cables you might be using, and make sure you've connected the headset to the correct port for your graphics card. If you're using any adapters, make sure they're compatible with Mixed Reality. If you're still having problems, try updating your graphics driver.** <br/><br/><ul><li>If you're using any custom modes or refresh rates on your PC monitor, try setting their refresh rates to 60Hz.</li><li>Make sure any adapters you are using support Windows Mixed Reality.</li><li>Try installing the latest graphics driver from the graphics card manufacturer's website.</li><li>Click "Try again" to see if it's a transient issue.</li></ul> |
| 14-4  / -             | **We ran into a problem connecting to your headset. Try removing any extension cables you might be using, and make sure you've connected the headset to the correct port for your graphics card. If you're using any adapters, make sure they're compatible with Mixed Reality. If you're still having problems, try updating your graphics driver.** <br/><br/><ul><li>Your PC may have more PC monitors connected than your graphics adapter can support. Disconnect all but your primary PC monitor.</li><li>Make sure any adapters you are using support Windows Mixed Reality.</li><li>Install the latest graphics driver from the graphics card manufacturer's website.</li><li>Click "Try again" to see if it's a transient issue.</li></ul> |
|   15-5  / -             | **Mixed Reality Portal has lost synchronization with core Mixed Reality and Windows components it depends on.**<br/><br/><ul><li>This could be caused by a performance issue with your PC. Make sure your CPU, GPU and HDD are not pegged in Task Manager.</li><li>Temporarily disconnect all other USB devices from your PC.</li><li>Restart your PC.</li></ul> |
|   -     / H0002000-0    | **Your PC's operating system has gotten into a mismatched state for Windows Mixed Reality**<br/><br/>Check Windows Updates for updates. |
|   -     / S0002261-101, S0002361-101 | **A problem with a Mixed Reality shell component is preventing Mixed Reality Portal from starting properly**<br/><br/><ul><li>Open the Application Log using Event Viewer on your PC to check for any application crashes at around the time you tried to start Windows Mixed Reality.</li><li>Make sure your graphics driver is up-to-date.</li><li>The HDMI adapter you are using is incompatible with Windows Mixed Reality. See the supported and recommended HDMI to mini display port (DP) dongle [here](recommended-adapters-for-windows-mixed-reality-capable-pcs.md).</li></ul> |