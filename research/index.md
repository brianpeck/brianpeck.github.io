---
layout: page
title: Research
tags: [research]
modified: 2014-08-12
comments: false
---

## Research Interests

* Wireless Networking and Communication
* Remote Situational Awareness
* Cloud Security

## Projects

As a Ph.D student at Iowa State University, I have had the opportunity to work on a variety of projects across multiple departments.

> ### Cloud Security

Most recently, my research has focused on cloud security as part of the Security and Software Engineering Research Center ([S<sup>2</sup>ERC][s2erc]) at Iowa State University.
Specifically, I am focusing on intrusion and fraud detection for web applications hosted in the cloud.

> ### Homunculus Camera

![homcam](/images/homcam.jpeg)
{:style="width: 200px" .image-pull-right}

#### HomCam hardware and software

The Homunculus Camera (HomCam) was developed as part of an ongoing research project with the Virtual Reality Application Center ([VRAC][vrac]) at Iowa State University.
The HomCam is a head mounted device which allows the live transfer of 360&deg; video to a remote viewer.
This allows the remote viewer to see what the HomCam wearer is seeing, as if they were inside the head of the wearer, hence the name [Homunculus][homunculuswiki] Camera.

The HomCam itself uses 4 cameras.
The four video streams are processed by frame grabbers before being broadcast over Wi-Fi.
To enable this, we designed custom software in `C++` to enable the streaming of the video.
The client is a graphical application which allows the viewing of all four streams simultaneously, and was developed with `Qt`.

#### User Study

Given the HomCam system, we then designed and conducted a user study to determine how useful it is.
Specifically, we studied the ability of participants to build spatial awareness of a foreign environment by having them identify targets and draw maps after viewing footage from the HomCam, both with a 360&deg; and a 180&deg; view.
The results of the study are still being analyzed and will be presented in a future publication.

##### Publications
* In progress.

> ### Power Save Mode with Adaptive Wakeup (PSM)

In an effort to reduce energy usage in wireless networks, most mobile devices use the 02.11 Power Save Mode (PSM) to put the wireless network interface card (NIC) to sleep when no data is being transferred.
However, this mode impacts packet delay, as devices cannot send or receive data when the NIC is asleep.
To this end, we designed Power Save Mode with Adaptive Wakeup (PSM-AW), which allows a mobile device to sleep for as long as possible, before adaptively waking up based on the current connection.
In this manner, a device can sleep as long as possible, without the risk for long delays.

We implemented PSM-AW by modifying the [Madwifi][madwifi] driver.
Our custom driver monitors the current connection statistics and selects a time to wake up the NIC for maximum performance or power savings, depending on the user's needs.

##### Publications
* **B. Peck** and D. Qiao. “A Practical PSM Scheme for Varying Server Delay”. *Vehicular
Technology, IEEE Transactions on*, In Press.

> ### Smart Access Point (SAP)

One of my first projects was the implementation of a Smart Access Point (SAP) which enabled seamless load balancing between multiple interfaces.
The SAP utilizes an OAMI (One-AP-Multiple-Interface) architecture to allow a single wireless AP to provide service to clients on multiple channels.
The SAP can then transfer clients between the two interfaces in an effort to maximize our Traffic Fulfillment (TF) performance metric, which seeks to quantify user experience.
Clients are transfered between interfaces through the use of the Channel Switch Announcement (CSA) management frame as defined in IEEE 802.11h.

SAP was implemented by modifying the [Madwifi][madwifi] device driver.
This modification required the addition of multiple custom modules at the kernel driver level, while also creating a user space application for coordination and monitoring.
Further details can be found in the [paper][sappaper].

##### Publications
* X. Chen, Y. Zhao, **B. Peck**, and D. Qiao. [“SAP: Smart Access Point with Seamless Load
Balancing Multiple Interfaces”][sappaper]. *INFOCOM, 2012 Proceedings IEEE*, pp. 1458–1466. 2012.

[madwifi]: http://madwifi-project.org/
[sappaper]: http://home.engineering.iastate.edu/~daji/papers/2012infocomc.pdf
[vrac]: http://vrac.iastate.edu/
[homunculuswiki]: http://en.wikipedia.org/wiki/Homunculus
[s2erc]: http://s2erc.iastate.edu/
