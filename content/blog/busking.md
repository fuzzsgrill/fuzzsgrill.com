+++
title = "Busking"
date = 2025-05-11
summary = "A true story on live lighting"
draft = false
layout = 'simple'
+++
Sooo the other night I had the opportunity to busk on an ETC EOS desk and let me tell you about it. For context busking is live light design.

I was apart of a concert, at a new company and they are running an IonXe 20. I will always go to it for cueing, even though it is not built for live stuff, when you get it set up right it is a power house in that too. Let me share my experience:

When I got to the venue they had ETC ColorSource Spot Vs, I knew that these were going to pretty fixtures. They were in 19 and 50 degree lenses, and were able to produce beautiful color. Nice and responsive too. I got them hung and cabled, I had to hook them into stage pin (three pronged connecters) and then take that into a True 1, then power jump (or daisy chain) them. True 1 to True 1, and DMX to DMX. DMX (digital multiplexing) is how the lights talk and to the things that they need to do, it is more complex but that is a topic for another day. Back to the Ion and the set up. 

I also put ETC ColorSource Pars that are pointed to the audience, just some nice crowd/back lighting. I also created an effect that will make them color change and then revert to their background state (or what they were doing before the effect was applied), something that a mentor taught me (he also showed me some tricks about the console). I also but gobos in, they were installed in two 50 degree lenses and they worked. They did great, and cooperated with me on what ever I asked them to do. 
This was more than enough light for the stage, now the hard part was the show file. 

I had to construct the show file so that it was able to be modified at a moments notice, and I had everything that I needed within reach. I could grab the Pars or the Vs that were sitting above us and then give them their instructions, strobing, color or how bright they were. I had to plan ahead on how I wanted things to work and how I wanted them to be set up. From turning them on at the press of a button to a color change. I also wanted the ability to time them, so instead of "snapping" on and off I could make them fade to whatever I wanted. 

I figured I should start by getting the patch together and then go from there. I can use a flash drive to pull the show file from the console, a perk of the EOS consoles. At the end of the day it is a Windows Computer. It is something that is becoming more and more common, even sound consoles do it. Some of them are using SD cards instead of USB but it is a concept that is adapted. I did a lot of work at home for this project and it was great. I was able to sit at my desk and build, what I ended up doing is grouping and fader mapping. This was the configuration at the end of it all that I settled on:
![The Direct Selects](/images/di_selects.png)

These are called Direct Selects. They are built so that I could grab a fixture at will, either by typing on the console or by touching them on the screen. At the top are color pallets, these were preset colors that I told the fixtures in advance.

![A lot of red](/images/cp_red.png)

Underneath are the groups, so I had first electric, second electric, the two 50s that were lighting half the room, the crowds and the gobos. Need to adjust the pars? One button tap or <Group 4> in the command line will give me control.

Under that were all the effect presets and the offset button so I could control how I wanted the effect to work. 

From there we hit intensity pallets, they were programmed to turn the lights on and off and I had set them up in increments of 25. Did I use them? No not really, I was using the scroll wheel on the console. 

Finally we hit the channels that I wanted in reach so I could gain fine control over the system. I did have some other things there, like turning on and off the lights power from a button, soloing them and other things that I did not use that much but still wanted on hand. 

The real star of the show was the fader wing, that was my go to for the whole show. 
![the faders](/images/twenty_faders.png)

I had color pallets mapped to them and submasters on them. As I needed them to be on/off or a color a fader flip would get the task done. Then on the faders labeled Global FX, they controlled how fast the effects and how deep they were working, the Man Time fader was how long I wanted things to fade in or out as I needed them too. If I needed a certain fixture to fade in, I could hit <1 @ Full> bring that Man Time fader up to 5 sec and 1 will come to Full in 5 Seconds instead of the default time.

I found out that 20 faders is not enough for what I had to do...so the next thing to do was use digital faders. 
![more faders](/images/mroe_faders.png)
Same concept as before, I mapped the Man Time twice on accident. The IP 22 Fader was all stage, S25 (the first yellow fader) was a preset look for the band needing to get themselves back together. The green fader was a failed attempt at something. S 13 was a preshow look that I liked and wanted to keep on hand. 
![rainbow colors](/images/rainbow.png)

S 26 was a look that I liked for a friend who sang "Strawberry Fields Forever" from the Beetles and the last one was a strobe effect that I did not want to reset every time I did it. The fixtures are not pleasant getting them to start strobing. They need to know their mode and then the speed vs the other way around. 
This was what I was looking at the whole time

![the thing I stared at](/images/the_thing_i_stared_at.png)

Complete and total chaos that I made it work. The nice part was no one knew what the design was (heck even I didn't know) so what ever happened it was nice. 

Do I recommend busking on an Ion Xe 20? 
Yes and No. Yes as in it is a good learning experience to know how its done, and a blast to do it, (as long as you have more physical faders on hand). No because it can be a bit tricky to set up, but worth the planning that goes into it. 