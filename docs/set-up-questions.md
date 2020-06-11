---
title: Setup FAQs
description: Advanced Windows Mixed Reality troubleshooting for setup questions that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Setup, Windows Mixed Reality Home, Windows Mixed Reality Portal
---


# Setup FAQs 

## My Xbox controller isn't working with Windows Mixed Reality.

* Make sure your controller is turned on, fully charged, and connected to the PC.
* Replace the controller’s batteries.
* If you're using a Bluetooth controller, go to **Settings > Devices > Bluetooth & other devices** on your PC and make sure it's paired (it should be listed on the page).

## I can't direct input (controllers, gamepad, mouse/keyboard) into Windows Mixed Reality.

When you put on your headset, input should automatically get toggled to your mixed reality experience through your headset's presence sensor. A blue bar should appear on your Desktop:

![Windows Desktop with input being directed to headset](images/1050px-windowsy.png)

If input doesn't get toggled automatically, you will need to manually toggle input to your headset. You can do this by typing **Windows Key + Y** on your keyboard (and the same to toggle input back to the desktop).

## The Mixed Reality Portal doesn’t open when I plug in my headset.

Mixed Reality Portal, the app that takes you through Windows Mixed Reality setup, is designed to open automatically when you plug in a compatible headset. If it doesn’t open, go to Start and type "Mixed Reality Portal" in the Search box to open the app. If you can’t find Mixed Reality Portal, that might mean you need to [update to the latest version of Windows](https://support.microsoft.com/en-us/help/12373/windows-update-faq).

## How do I choose between "Seated and standing" and "All experiences"?

If you choose "Seated and standing", either during headset setup or later on, you'll be using your headset without a boundary. You can sit down or stand up, but you'll otherwise need to stay in one place, as you’ll have no boundary to help you avoid physical obstacles. Some apps might be designed to work with a boundary, so you might not be able to use them or you might not have the same experience if you use them without a boundary. See ["What's a boundary and why should I create one?"](boundary-questions.md#whats-a-boundary-and-why-should-i-create-one).

If you choose "All experiences", you'll set up a boundary and you can use apps and experiences that work with a boundary as well as those that don't require one. 

## Learn Mixed Reality didn't run on first launch, and I went right to Windows Mixed Reality home.

You can re-run the learning experience by following the [re-run steps](learn-mixed-reality.md#how-do-i-re-run-the-learning-experience). 

## My controllers aren't showing in my Windows Mixed Reality home.

Make sure your controllers have full batteries and that they are paired correctly using Bluetooth. Try powering the controllers off and on using the Windows Button. If you still cannot see your controllers, try in-pairing and re-pairing each controller in the Settings menu under **Devices > Bluetooth**.

## The floor of my Windows Mixed Reality home doesn't appear to be at the correct height, or it is slanted.

Select **Start > Room Adjustment** which will launch once you place the app in the world, to make changes while wearing your headset. In this app, you will be directed to use the touch pad (motion controller) or direction pad (gamepad) to adjust the floor height. When the floor feels correct, use the Windows button to return to your home.

## My headset has stopped tracking.

Make sure the lights are on and that there isn't anything obstructing the inside-out tracking cameras on the front of your headset. If tracking is lost, it can take a few seconds to resume. If tracking does not resume, try restarting the Windows Mixed Reality Portal. See [Tracking system problems](tracking-problems.md) for more details.

## I can't show a preview of what I'm seeing in my headset on my desktop.

Windows Mixed Reality Portal has a **Play** button at the bottom of the screen that allows you to show a preview of what you're seeing in your headset on your desktop screen. But for performance reasons, this feature is only available on PCs running at Windows Mixed Reality Ultra (90Hz).

## I got a "Something went wrong" error message, or I'm having problems in the Mixed Reality Portal.

Restart Windows Mixed Reality:
1. Disconnect both headset cables from your PC.
2. Restart your PC.
3. Reconnect your headset.

If that doesn't work, make sure that your PC recognizes your headset:
1. Select Start.
2. Type "Device Manager" in the search box and select it in the list. 
3. Expand "Mixed reality devices" and see if your headset is listed. 

If it isn't listed, try the following:
1. Plug the headset into different ports on the PC, if available.
2. Check for the latest software updates from Windows Update.
3. Uninstall and reinstall Windows Mixed Reality:
    1. Disconnect both headset cables from your PC.
    2. Select **Settings  > Mixed reality > Uninstall**.
    3. Select **Settings  > Devices  > Bluetooth & other devices** to unpair your motion controllers. Select each controller, and then select "Remove device".
    4. Plug your headset back into your PC to reinstall Windows Mixed Reality.

