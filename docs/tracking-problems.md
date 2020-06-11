---
title: Tracking FAQs
description: Advanced Windows Mixed Reality troubleshooting that goes beyond our standard consumer support documentation.
ms.topic: article
keywords: Windows Mixed Reality, Mixed Reality, Virtual Reality, VR, MR, Troubleshoot, Errors, Help, Support, Tracking
---


# Tracking FAQs

## The system cannot find the boundary and I'm being presented with setup UI.

This means that the tracking system was unable to recognize your environment. If you are in a new environment, you must set up the [boundary](https://docs.microsoft.com/windows/mixed-reality/enthusiast-guide/set-up-windows-mixed-reality#set-up-your-room-boundary). If you have previously used the device in this environment and set up a boundary:
* Make sure the room has enough light.
* Make sure you have worn the device and looked around the room. The device must observe your environment to know where it is. It will not find your bounds if it is sitting on a desk or table.
* Unplug the device, close Windows Mixed Reality, and plug the device in again.
* Something may have changed in your environment and the device no longer recognizes it. Try setting up a new boundary.

If these steps do not resolve the problem, then delete your environment data and set up the boundary again.

## The system is presenting me with UI that asks me to choose setup for all experiences or seated/standing, and I see my bounds.

The device is taking too long to find the bounds. You can bypass this message by choosing the option to use a boundary and you will be taken to your Windows Mixed Reality home with your bounds present.

## I often see a message saying "I've lost my bounds".

The tracking system is having a hard time tracking and identifying your environment. In this state, the device can no longer display your bounds and the headset switches to 3DOF to keep you from to bumping into things in the real world until it locates your bounds again. To fix this:
1. Make sure that the room has enough light.
2. Rerun the setup if you recently redecorated or remodeled the room.
3. Unplug the device, close Windows Mixed Reality, and plug it in again.
4. Clear your environment data and set up the device again.
5. If the message persists, contact customer support.

## I can look around but I can't translate (I'm stuck in 3DOF).

This means that the tracking system cannot generate pose, or the application has stopped using new pose data to render. Check the following:
* Make sure the room has enough light.
* Make sure the room has enough details to track.
* Unplug the device, close Windows Mixed Reality, and plug in the device again.
* If the message persists, contact customer support

## The view in the HMD is completely frozen.

This usually means the application or a system level component has failed. Try to:
1. Press the "home" button to leave the application.
2. Unplug the device, close MRP and plug the device back in.
3. Reboot the PC.

## I frequently see a black border around the view in the headset. Sometimes it's like I'm looking down a tunnel.

This means that the application is not able to hit frame rate on your PC and the system is using old frames to render the view in the headset. Since applications only render the part of the world you are looking at, if they do not consistently hit their frame rates, then the system will attempt to continue to render the world from a previous point of view and will fill in the missing details with black. If this happens frequently:
1. Close or terminate all unneeded programs to free up memory and CPU.
2. Reduce detail settings in your application.
3. Go to **Settings > Mixed Reality > Headset Display** to reduce the amount of detail shown in the Windows Mixed Reality home.

## The view in the headset is jittering and stuttering a lot.

It is likely that the system is not able to render content to the headset, or the tracking system is experiencing problems. Check the following:
1. Open "Task Manager" to make sure that your PC has enough compute resources (for example, you should have 80% of CPU free, 400MB of RAM, and disk IO should be below 80%).
2. Make sure you have the latest graphics drivers for your hardware. See the [graphics driver section](before-you-start.md#make-sure-you-have-a-compatible-graphics-driver).
3. Make sure the room has enough light.
4. Unplug the device, close Windows Mixed Reality, and plug the device in again.
5. Reboot your PC.
6. If the problem persists, contact [customer support](https://support.microsoft.com/).

## The world briefly froze and perhaps tilted or flipped upside before returning to normal.

This could be caused by an application or system level component hitting a fatal error, or a temporary lack of memory or CPU resources. Check the following:
1. Open "Task Manager" and ensure that at least 20% of the CPU is free and 400MB of memory is available (for example, you should have 80% of CPU free, 400MB of RAM, and disk IO should be below 80%).
2. Go to **Event Viewer > Windows Logs > Application** to look for any errors from around the time of the freeze. Look specifically for anything that refers to HololensSensors, Mixed Reality, or the application that you were running around that time. Those logs might explain what caused the failure.
3. Reboot the PC if the problem persists.

## The world flipped upside down momentarily and returned to normal.

This is typically caused by errors in obtaining sensor data from the headset to inform the tracking algorithms. If this happens frequently:
1. Plug the headset into a different USB 3.0 port.
2. Plug the headset directly into the PC rather than into a USB 3.0 hub.
3. If the problem persists, contact [customer support](https://support.microsoft.com/).

## The world is tilted but I can navigate and walk around in Windows Mixed Reality.

Sensor data errors being recorded into the environment data that is stored on your PC can cause Windows Mixed Reality to appear tilted, sometimes permanently. To fix this:
1. Unplug the headset, close Windows Mixed Reality and plug the headset back in.
2. Reboot the PC.
3. Clear your environment data.

