---
title: How to uninstall Windows Mixed Reality
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Uninstall
---


# How to uninstall Windows Mixed Reality

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
