Shipping one UI to three platforms at once (Windows, Android, iOS)

<p>The first thing on screen after launch:

![poster](./img1.png)

The exercise links an emulator to a web server that runs on the local host, through a public relay.

Fetch the relay tool from PowerShell:

    PS>> wget install Microsoft.relaytool

Authorize the account, then publish the port:

    relayctl user login -g
    relayctl host -p 5000 --allow-anonymous

The console then reports where the service can be reached:

    PS E:\lab\src\webapi> relayctl host -p 5000 --allow-anonymous

    Port bound: 5000

    Public endpoints are published under the assigned subdomain

    Traffic inspector sits beside them

    Waiting for inbound connections

Edit a source file and save it.

![poster](./img2.png)

Run again and the handshake between emulator and server is visible:

![poster](./img3.png)

The first view the host presents while validating the relay:

![poster](./img4.png)

Then this one:

![poster](./img5.png)

Every flag is spelled out on this page: https://blog.example.dev/relay-flags

License: MIT