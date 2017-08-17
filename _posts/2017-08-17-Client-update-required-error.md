---
title: Client update required error
description: How to solve the client update required error in Rust
header: Solve the client update required error in Rust
---


Today is a thursday and as expected a new update of 385mb hit Rust. Now ideally a normal update of the server should have been a smooth affair.

But, it didn't quite go that well.

We have a cronjob running on our server that checks for updates every 10 minutes and makes sure that the server restarts in case a new update ships.

At around 1:35am IST, the update got completed and as always the server restarted. There were about 3 - 4 people on the server before the update had sstarted. When I saw that my server's update has got completed I messaged them to connect back to the server.

but 

this is what I saw in the console

````
kicking player name, their protocol is 2007 not 2008
````
which sounded quite absurd to me as I had already updated my server.

Solution:

The problem was that the server had got updated but the client on their side had not. Even restarting steam and Rust did not help. Finally I had to
follow this process to get my game working

````
Go to Steam > settings > clear download cache
````

Once steam was restarted after that I got the full update on my machine and was finally able to connect back to my server.
