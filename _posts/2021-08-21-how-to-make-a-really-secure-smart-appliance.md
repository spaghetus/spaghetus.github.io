---
layout: post
author: Willow Carlson-Huber
tags: security
---

TL;DR: Assume your hardware will last, and trust the user and suspect everything else, including your own infrastructure.

Connected devices can make life very convenient, and there's an undeniable cool factor involved. However, in many cases they are designed without security in mind. A family friend recently had a scare involving a smart baby monitor where an unknown third party was able to converse with their child during the night using the baby monitor's speaker and microphone. This is, of course, unacceptable, and it inspired me to get up on my soapbox and tell y'all how it's done.

As I hope you'll realize, although making a secure smart device is hard, it's far from impossible. 

<img src="https://images.unsplash.com/photo-1522881451255-f59ad836fdfb?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDJ8fHdyaXRlfGVufDB8fHx8MTYyOTQ4OTU1Mw&ixlib=rb-1.2.1&q=80&w=2000" title="An image of a person's hands writing in a notebook on a desk. Photo by NeONBRAND / Unsplash." width="500">

Flashing by the end-user is critical to a device's longevity. A device cannot remain safe to use unless it remains secure, and what's secure today may not be secure tomorrow. This process has to be easy and robust, so end-users will actually be able to do it without bricking their system, and it must trust the end-user - checking images against your signature defeats the purpose of allowing it.

There must also, of course, be software for end-users to flash their hardware with. Unless you gain some kind of cult following, your users won't bother reverse-engineering your hardware. As a result, failure to publish your source code and documentation also greatly limits your device's useful life.

Delivering automatic updates from the backend is still critical for security, but they should not be silent - the user should consent to each update, and there should be a robust method for rolling back from malicious or broken updates.

(P.S: If any of the software shipped on your device is licensed with LGPLv3, you are required to allow the end user to modify the software on their device and document the required steps to do so.)

<img src="https://images.unsplash.com/photo-1512309739986-032cbacdb618?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDl8fGtleXN8ZW58MHx8fHwxNjI5NDg5NjUz&ixlib=rb-1.2.1&q=80&w=2000" title="An image of a wall with many keys on hooks. Photo by Chunli Ju / Unsplash." width="500">

Encryption isn't a surprising feature, but trustless design and out-of-band exchange might be - hopefully you'll see why I think it's so important.

Encryption of some kind is required for a device to be considered secure. The user must be able to verify information sent by the product, the product must be able to verify information sent by the user, and all such information must be encrypted. This prevents information from being intercepted and collected or modified.

<img src="https://images.unsplash.com/photo-1464316325666-63beaf639dbb?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwxMTc3M3wwfDF8c2VhcmNofDN8fGZyb250JTIwZG9vcnxlbnwwfHx8fDE2Mjk1NzczNDA&ixlib=rb-1.2.1&q=80&w=2000" title="An image of a yellow door. Photo by Evelyn Paris / Unsplash." width="500">
