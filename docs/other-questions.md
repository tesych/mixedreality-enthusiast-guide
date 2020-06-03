---
title: Other questions
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Uninstalling Windows Mixed Reality, Supported Languages
---

# Other questions

## My Samsung Odyssey or Odyssey+ headset firmware update is getting stuck.

Samsung owns and publishes headset firmware updates delivered via their "Samsung HMD Odyssey Setup" and "Samsung HMD Odyssey+ Setup" Device Companion apps. For more details and for help with Samsung firmware update issues, please reach out to Samsung Customer Service.

If the firmware update process is getting stuck, and there has been no progress for more than five minutes:
* Unplug all of your other USB devices temporarily and retry the firmware update.
* Connect your Samsung headset to a different USB 3.0 port on your PC.
* Disabling and/or uninstall any software installed that may interfere with firmware updates, like Gigabyte's AORUS App Center.
* Use a different PC to perform the Samsung headset firmware update.

## How do I access my PC desktop in Mixed Reality?
You can access your PC desktop in Mixed Reality using the Desktop app. Launch it in the headset from **Windows Button > All apps > Desktop**. 

## How can I see multiple monitors in Mixed Reality?
By default, Desktop app automatically switches to display the monitor with focus. If you want to see all of your monitors in Mixed Reality: 
* Click the monitor icon on the top left corner of the app
* Disable "Automatically Switch Monitor"
* Pick the monitor you want to see
* Launch another instance of the Desktop app
* Pick the monitor you want to see on that instance 
* Repeat for all of your physical monitors 
Note that you will have to reselect the monitor to show on each Desktop app every time you restart Mixed Reality. 

## My Desktop app only shows a black screen.
If your PC has an Nvidia hybrid GPU, the issue may be caused by Nvidia device running the runtimebroker.exe on the discrete GPU instead of the integrated one. To fix this issue, follow these instructions under "[How do I create Optimus settings for a new program?](http://nvidia.custhelp.com/app/answers/detail/a_id/2615/~/how-do-i-customize-optimus-profiles-and-settings%3F)" to add C:\windows\system32\runtimebroker.exe and force it to run on the "Integrated graphics" processor. 

## My Wi-Fi slows down when I'm using Windows Mixed Reality.

If you're using a 2.4GHz Wi-Fi connection, your motion controllers might slow down your Wi-Fi. Try one of the following:
* Switch to a 5GHz Wi-Fi connection, if one is available. [Learn more](https://support.microsoft.com/en-us/help/4000461).
* Use a separate Bluetooth adapter to connect your motion controllers to your PC. See [recommended adapters](https://support.microsoft.com/en-us/help/4039260/windows-10-mixed-reality-pc-hardware-guidelines).

## I got a message that said to plug in and charge my PC. Why?

If you're using a laptop, Windows Mixed Reality works best when the PC is both fully charged and plugged in. 

## What is the Experience options setting?

The Experience options setting (**Settings > Mixed reality > Headset display > Experience options**) allows you to change the Windows Mixed Reality performance settings. This enables you to choose the best possible experience for your hardware configuration across a range of content. The 90Hz experience is available to all systems, but you might want to try Automatic to see which setting you prefer. Here are the options:
* Automatic: Windows Mixed Reality will determine the best experience for your hardware configuration. For most people, this is the best choice to start with.
* 60Hz: Sets the refresh rate to 60Hz and turns off certain features, such as video capture and preview in Mixed Reality Portal.
* 90Hz: Sets the refresh rate to 90Hz.

## What languages are supported in Windows Mixed Reality?

Windows Mixed Reality is available in the following languages. If your PC is set to a different language, you can still use Windows Mixed Reality, but the interface will appear in English (United States), and speech commands and dictation won't be available.

* Chinese Simplified (China)
* English (Australia)
* English (Canada)
* English (Great Britain)
* English (United States)
* French (Canada)
* French (France)
* German (Germany)
* Italian (Italy)
* Japanese (Japan)
* Spanish (Mexico)
* Spanish (Spain)

The Windows Mixed Reality onscreen keyboard is English (United States) only. To enter text in another language, use a physical keyboard connected to your PC. You can also use dictation in one of the supported Windows Mixed Reality languages listed above—just select microphone on the onscreen keyboard.

Windows Mixed Reality is also available in the following languages without speech commands or dictation features:

* Chinese Traditional (Taiwan and Hong Kong)
* Dutch (Netherlands)
* Korean (Korea)
* Russian (Russia)

## I have questions about my headset hardware.

For details about your headset, check with the manufacturer. There may be a product guide in the box, or you can try the manufacturer’s website.

## How do I uninstall Windows Mixed Reality?

1. Disconnect your headset from your PC.
2. Close Mixed Reality Portal.
2. Go to  **Start > Settings > Mixed Reality** and select "Uninstall".

When you're ready to start using your headset again, plug it in, and Mixed Reality Portal will take you through setup.

## I got a "We couldn't finish uninstalling Windows Mixed Reality" message.

This means that some files, including information about your environment, might still be on your computer. This can cause problems if you decide to reinstall Windows Mixed Reality later. You can manually remove any remaining Windows Mixed Reality info from your PC by modifying the registry and using Windows PowerShell to run commands. _If you modify the registry incorrectly, serious problems might occur. Make sure to follow these steps carefully. For added protection, back up your registry before you modify it so you can restore it if a problem occurrs._ For more info, see [How to back up and restory the registry in Windows](https://support.microsoft.com/en-us/help/322756/how-to-back-up-and-restore-the-registry-in-windows). 

To uninstall Windows mixed reality using these commands:
1. Restart your PC.
2. In the **Search** box, type "regedit" and then select **Yes**.
3. Remove the following registry values:
   <ul>
    <li><b>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Holographic</b>, then delete <b>FirstRunSucceeded</b>.</li> 
    <li><b>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Holographic\SpeechAndAudio</b>, then delete <b>PreferDesktopSpeaker</b> and <b>PreferDesktopMic</b>.</li> 
    <li><b>HKEY_CURRENT_USER\Software\Microsoft\Speech_OneCore&gt; Settings\Holographic</b>, then delete <b>DisableSpeechInput</b>. Note:the registry items in HHKEY_CURRENT_USER must be deleted for every user account on the PC that has used Windows Mixed Reality.</li> 
    <li><b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\PerceptionSimulationExtensions</b>, then delete <b>DeviceID</b> and <b>Mode</b>.</li> 
    <li><b>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Holographic</b>, then delete <b>OnDeviceLearningCompleted</b>.</li> 
   </ul>
4. Remove the following registry keys: 
   <ul>
   <li> <b>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\HoloSI</b></li> 
   <li> <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\HoloSI</b></li> 
   <li> <b>HKEY_CURRENT_USER\Software\Microsoft\Speech_OneCore\Settings\HolographicPreferences</b></li><br/></ul>
5. Close the Registry Editor.
6. Navigate to **C:\Users\user name\AppData\Local\Packages\Microsoft.Windows.HolographicFirstRun_cw5n1h2txyewy\LocalState**, and then delete **RoomBounds.json**. Repeat this for each user who has used Windows Mixed Reality.
7. Open admin cmd prompt and navigate to **C:\ProgramData\WindowsHolographicDevices\SpatialStore\HoloLensSensors**. Then delete the contents of the **HeadTracking data** folder (but not the folder itself).
8. Type "powershell" in the **Search box**, right-click **Windows PowerShell**, and then select **Run as administrator**.
9. In Windows PowerShell, do the following:
   <ul>
   <li>Copy and paste the following at the command prompt, then press Enter: <b>Dism /online /Get-Capabilities</b></li> 
   <li>Copy the Capability Identity that begins with Analog.Holographic.Desktop (if it isn&#39;t there, that means this item isn&#39;t installed. In that case, skip to step 10 ).</li> 
   <li>Copy and paste the following command prompt, then press Enter: <b>Dism /online /Remove-Capability /CapabilityName:the Capability Identity copied in the last step</b></li>
   </ul>
10. Restart your PC.
