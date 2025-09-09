the code I gave will work between different devices and different browsers as long as:

Both users are connected to the internet

Both open the same HTML file (hosted online or sent to them)

One user shares their PeerJS ID with the other

The other user enters that ID and clicks Call

How it works (in simple terms)

This uses WebRTC with PeerJS:

WebRTC = a technology that allows two browsers to send audio, video, and data directly to each other (peer-to-peer) without passing through a central server for streaming.

PeerJS = a small JavaScript library that makes WebRTC easier to use. It has a free signaling server that helps the two peers find each other.

Step-by-step process when you run the code

User A opens the page → The browser connects to PeerJS's free cloud server and gets a unique ID (shown on screen).

User A sends this ID to User B (via WhatsApp, email, etc.).

User B opens the page → enters User A's ID into the box → clicks Call.

PeerJS server exchanges "connection information" (called signaling).

The two browsers create a direct encrypted connection and send audio/video streams between them.

Important notes

It does not require the same browser — Chrome, Firefox, Edge, Safari all work.

It does not require same network — you can connect from different cities or countries.

It does not require a backend unless you want to scale up or run your own PeerJS server.

This basic version is for 1-to-1 video calls. For multi-user calls (like Zoom), we need extra code to handle multiple streams.
