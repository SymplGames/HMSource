*WARNING* I FORGOT TO MULTIPLY THE MOVEMENT CODE BY DELTA SECONDS. THIS CAN CAUSE SOME ISSUES. I'LL HAVE IT FIXED WHEN I GET TIME!

I decided to start getting into game development, and my friend suggested that I try this out first.

The goal was to get an idea of how Unreal Engine works with some basic fundamentals. 

I'll be working on more complex projects and uploading them here as well.

I thought this project was pretty cool because of how the runner moves through the track. 

Instead of simply falling or moving forward, the runner navigates to a nav point within each tile.

This lets you generate a track using any shape you want.

The current method is pretty dumb, because I haven't figured out how to use nav mesh in an infinite world yet.

This means that if the points don't line up correctly, the player will be forced into a wall because they just move to the next nav point without checking collisions.

The tunnel is generated by BP_TileManager and generates a series of start tiles. After the player begins to overlap the end point, a new tile is created at the last tile recorded by the tile manager.

Each tile uses a base class with special child classes that can do whatever you want them to. 

By default I added a few moving platforms and a simple pickup spawner. 

There is a pickup class that gives the player coins.

The player contains some functions that can be extended for extra gameplay elements if you'd like.

I tried to setup networking, but I don't think an endless runner is a good place to start. 

I might use the tile manager to generate a pre-defined track, where the players would race each other but that's a little too much for me right now.

Let me know what you think. I hope this helps someone either learn something cool, or make a fun game!

Thank you for your time and have a great day!
