+++
title = "Entota WebSocket Firewall Requirements"
Weight = 6
+++


Entota uses the WebSocket protocol for a few different features, mainly
centered around the deep guidance module. The WebSocket protocol has
some required HTTP headers that aren't commonly used and tend to be
stripped out by corporate firewall software. Below is an example of a
BOA app client initiated WebSocket request to BOA cloud, and the
response back to the client. All of the headers outlined in this example
are required.

**Request**

GET wss://api.igc-prd-na2.boa.ninja/events HTTP/1.1

Host: api.igc-prd-na2.boa.ninja

Connection: Upgrade

Upgrade: websocket

Origin: https://igc.boaweb.com

Sec-WebSocket-Version: 13

Sec-WebSocket-Key: x3JJHMbDL1EzLkh9GBhXDw==

Sec-WebSocket-Extensions: permessage-deflate; client\_max\_window\_bits

**Response**

HTTP/1.1 101 Switching Protocols

Date: Tue, 03 Apr 2018 15:03:00 GMT

Connection: upgrade

Upgrade: websocket

Sec-WebSocket-Accept: HSmrc0sMlYUkAGmm5OPpG2HaGWk=

It appears as if the header "Sec-WebSocket-Protocol" is also part of the
WebSocket specification (even though BOA doesn't use it), so it may be
wise to add that to the Allow list to fully support the WebSocket
protocol.

By allowing these headers through the firewall, Entota's deep guidance
feature works as expected.

**NOTE**: It is recommended that you use Google Chrome to perform the
steps below.

To verify that the WebSocket upgrade is successful:

1.  Navigate to the Entota landing page and log in to Entota with a
    valid user name and password.
2.  Open the Developer Tools in Chrome by going to the **kebab-menu (the
    3 vertical dots in the top right) \> More Tools \> Developer
    Tools**.
3.  Click the **Network** tab.
4.  Type the text "**events**" into the **Filter** field to display the
    request that uses the WebSocket protocol.
5.  In Entota , on the Jump to... menu on the right, select **Term** to
    get a list of terms in your Entota system.
6.  Select any of the terms.

    **NOTE**: Once you select the term, the "events" request displays on
    the Network tab of the Developer Tools panel.

7.  Select the "events" item in the list and the details of that request
    display to the right of it.
8.  Click the **Headers** tab.

    **NOTE**: If the WebSocket upgrade was successful, the Status Code
    value has a green LED and reads "101 Switching Protocols." Click the
    **Frames** tab to view the actual WebSocket messages being sent and
    received over the socket. The term highlighting feature of deep
    guidance is now functioning correctly within the Term window.

If any other Status Code value displays, the WebSocket upgrade failed,
likely due to missing (stripped out) headers.
