+++
title = 'Mod Packs'
date = 2024-11-16
summary = "A mod pack for all you basic Minecraft needs!"
draft = true
layout = 'simple'
+++

This week I got to experience something of interest. I created a mod pack, “what started this?” You may ask, I decided to play some vanilla Minecraft to see what the new version hype that always happens was about. I am used to playing on a modded Minecraft server with my friends, this server has 300+ mods that make the game something different. When I spun up the Vanilla instance, I tried to use some of the mods that didn’t exist… You can imagine how that went for me. So, what did I do? I decided to create an overcomplicated solution to something that should not be an issue (this is how my brain is) 
I created a mod pack with some things that I think should be in vanilla. This pack had mods like Jade, JEI, improved animations, and shaders, and some other quality game essentials (downloadable at essentials.fuzzsgrill.com). When I started to investigate this install, I saw that I could use Modrinth for it. It's super easy and should be good to go… Well, after some trouble, I decided to make the app do it. A good friend/software dev saw me using Modrinth on Discord and asked what I was up to and I told him createing a mod pack for the necessities. 
I was able to get the mod pack created and running, when I saw how bad it was running I gave it more RAM to use as Modrinth auto-allocated to about 2 gigs of RAM. When I adjusted it, the game was constantly crashing so I decided to give up on that pack and create a new one. Shopping around on Modrinth is something of interest, you have most mods imaginable, it is nice too as Modrinth will download dependency mods if needed. When I was done, I sent it to my brother, for him to check out. This next part I am not sure how it happened, but I was on a call with another good friend and we somehow brought up ducks and Minecraft. I told her I added ducks to the game (via the modpack Ducklings). When she said “I got to see this” I decided to send her the pack so she could see it for herself, along with a screen shot with a raft of ducks happily quacking and floating around.

![ducks floating](/static/images/ducky.jpg)

I even captioned it with “They love bread”. My software developer friend chimed in with a system called Packwiz, a better way to distribute these modpacks, plus the server that I play on uses Packwiz for its distribution. He sends me a link to its documentation and I get started that next night. 
Oh wow that was interesting…
I use a system called Windows Sub Linux which essentially puts the Ubuntu terminal in Windows’s PowerShell. An amazing tool, I am not a minor stranger to Linux but I want to get better with it so I go with it. 
I could not figure out how to get WSL to get Packwiz installed, I called on my friend and he helped explain it to me and install it. It turns out we needed to use the wget command to followed by the Linux URL to install it. Once it got installed, he showed me around. I get started with it. I created and CD into new directory for the mod pack, then typed ```packwiz init```, to begin set up. After asking me some questions it created the pack.toml and index.toml. With those in hand we set up a Netlfiy system to deploy this. Then mods were added and off everything went. I got stuck a lot during the way due to the documentation being written in a strange way. Luckily my friend is an expert in this and helped me through the setup. The part that I got lost on was adding the URL that the pack.toml was located it at. I forgot that the Netlify deploy was that toml file. With that updated knowledge I updated the URL that was needed, and everything worked. There were some minor difficulties as I downloaded a bootstrap file twice, and entered the wrong command. Sent the errors to my friend and then immediately fixed them as I found what was wrong, a bit embarrassed I messaged him back with “fixed it lol” and a screenshot of the home screen of Minecraft. 
He laughed and then explained the art of rubber ducking where developers have little rubber ducks on their desks to help debug their code and he served as my duck. Now that everything is good to go and working I deploy it to Google Drive and figure out how to create it as an auto download and a much prettier URL. 

Without further ado here is what happened (in WSL)
1.	Make sure that you have Go and Git installed
2.	Use Wget and the linux URL to install Packwiz 
3.	Create a new directory and CD into it make sure that it is named something you can remember (i.e. Minecraft_mods_1.0)
4.	Type ```Packwiz init``` to the command line to activate Packwiz and create the mod pack
5.	Go to Modrinth and pick out mods that you want, as you choose them, enter the following command into the command line ```packwiz modrinth install  ___``` after install put the mod pack name or the direct URL
6.	It will install all the necessary mods that are needed including the pack. If you used the name of the pack, choose the pack that you want (it will number them asking which one you want) 
7.	Make sure you commit and push to GitHub often (and use branches)
i.	Git checkout -b “branch name (del quotation marks) 
b.	Git add .
c.	Git commit -m “example message (keep quotation marks)”
d.	Git push origin branch_name 
8.	When you are satisfied with your branch merge it to main with 
a.	Git merge origin main
9.	When you are done move on to Deploy:
Deploying:
Here things are going to get strange:
You will want a GitHub and Netlify account 
In Netlify click on Add new site and import an existing project and choose Git Hub 
![Picture of Netlify config](/static/images/Netlify%20config.jpg)

Sign into GitHub and choose your repo
Scroll down to branch to deploy and make sure it’s set to main and set base directory to / 

![Netlify inputs](/static/images/Netlify%20input.jpg)

Then hit deploy under everything. This will deploy your main github branch, copy that url. 

Then use Prism or Multi MC and spin up a new instance and choose your Minecraft version and what mod loader you are using, Fabric, cloth etc, under custom commands enter "$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://[your-server]/pack.toml” replace the URL with the one you got from Netlify.
You will also want to grab this boot stap file, https://github.com/packwiz/packwiz-installer-bootstrap/releases 
Move that to you instance Minecraft folder (it will appear after you hit ok). An easy trick to find your instance folder is to hit folder with the instance selected. Grab that boot strap file that you downloaded earlier and move it there. Now everything should be good to go, press launch and start playing.

If you want to share your modpack with others use the export function in prism and send that to them. The pack will auto-download and update whenever there is a change. 
