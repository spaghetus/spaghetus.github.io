---
layout: post
author: "Willow Carlson-Huber"
tags: "security"
---

I've had this idea in the back of my mind for a few years now, but I've never managed to actually make it. TL;DR: Almost all messengers available today have some serious trust issues.

Most messengers place some fundamental trust in their authors, which makes them very vulnerable to attacks.

* Fully trustful messengers like Discord, GMail, or your phone's SMS send your messages in plaintext through the author's hardware. This makes them vulnerable to attacks on privacy and reliability: your messages can be easily read and modified, you and the recipient can be easily identified, and a message's transmission can be easily halted.
* Partially trustless messengers like Signal or ProtonMail send your messages as ciphertext through the author's hardware. This protects them from attacks on the privacy of the message's content, but remains vulnerable to attacks on the privacy of the connection and the reliability of the transmission: Your messages can't be read or modified, but it's easy to identify the members of the conversation and to prevent its transmission.
* A fully trustless messenger would send messages as armored ciphertext through hardware owned by multiple independent organizations, all of which are unaffiliated with the author, and would pass the messages through multiple layers of indirection. This protects the privacy of the content through encryption, the privacy of the connection through indirection, the reliability of transmission through redundancy, and even the privacy of one's usage of the software itself through data armoring.

The concept protocol which I've named Courier fulfills the conditions for a fully trustless messenger. It does this using several components.

* Caw, which would armor data using a simple time-sensitive substitution cipher, replacing each 16-bit word of a message with a human word using a pseudorandom shared mapping. Randomly chosen meaningless words and punctuation would also be inserted. Messages would be split and numbered when a character limit requires it.
* Owl, which would encrypt and decrypt messsages using an as-yet-undecided quantum-resistant cipher.
* Birdsong, which would perform real-time physical information exchange using light, sound, external storage, or NFC.
* Parrot, which would communicate with third-party services for information transport using adapters compiled to WASI.
* Flock, which would manage the database of contacts, conversations, and secrets.
* Swallow, which would host an ephemoral Tor hidden service to allow transmission of large files at a high airspeed.