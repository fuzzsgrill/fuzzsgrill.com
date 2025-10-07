+++
title = 'Minty Desktop'
date = 2025-10-06T20:24:23-06:00
draft = false
summary = 'Linux Mode Activated'
layout = 'simple'
+++
I recently put Linux Mint onto my desktop computer (it's part of the reason why I have been gone for a bit, along with some other stuff) and it has been an interesting process to say the least. 

To start I was running Windows 11 (still am) and was sick and tired of all the shenanigans that Windows will cause. I still remember the days of Windows Xp, a legendary OS that can't do a ton today. When I first tried Linux, I did it with Ubuntu a Debian based distro and that failed horribly. 

I would boot from a USB with Ubuntu installed and I messed up partitioning. I accidentally did something to my Windows install. I would reboot the computer and then go into Windows to check something and every time I did that it would start to complain about my PIN being broken and every time I had to reset it. 

I ended that attempt by staying on Windows. A few months later I tried again and this time the computer would not boot off the USB drive and would throw out a PCIE error every time. That was the end of that attempt. A few more months later I try again. Somewhere in there I switched off of Ubuntu and over to Mint. I had a bad experience with Ubuntu when I tried it on my laptop. 

I booted off the USB from the BIOS and into Mint. I got hung up when I was asked to set up the drive. Here is some context on what my computer is. 
1. It is a free computer that I rescued from a company
2. It is a heavy machine
3. It has a Samsung SSD for boot (500gbs)
4. It has a WD Black M.2 drive that holds games (1TB)
5. It has a 2TB Seagate HDD for spare storage

What was happening was the Mint installer was not seeing the 500 gig SSD, that Windows has. It kept going to the HDD. I have worked with a HDD as a boot drive and it is a bad idea. They are slow to work with and yet super reliable. When I tried to get the system off of that HDD it failed completely. It would not let me go over to the SSD, or the M.2. I tried to remove the drive, it can't get to something that is not plugged into right? No luck, it was still on the wrong drive. Somewhere in here I decided to have the M.2 be the Linux boot drive instead of the SSD. The only reason why the M.2 is not the boot drive is because it is a new drive that I got for Christmas after the computer was set up. I tried super hard to get the M.2 to be a boot drive. This had me pulling out the HDD and the SSD. I removed the HDD from the computer while it was off. I pulled the SSD from it while it was on. That did get me to the M.2 drive and then when I saw that I had to partition manually I decided to stop and wait for my friend who is an expert in this. I stopped before I was going to do something dumb. 

 Yet, I already did something dumb. See the part where I pulled the SSD from the running computer? Yeah that destroyed my EFI boot partition for Windows. I spent an hour fixing my error. Doing all kinds of different things, getting Linux to fix it and I was about to reinstall Windows until I found myself into a Windows recovery area. That told me that there was a Windows install on the disk just not accessible to me. After poking around the menu I saw that I can use a restore point. 

This is where past me is helping out current me. That 2 TB HDD that I was being strange with? That holds a snapshot of my Windows drive with a recent restore point. I decided to give it a try and I got Windows back. With a breath of relief I decided to stick to Windows until I can get some help. 

A few days later my friend guided me though the Linux install. Fuzz, how did he see the install process? Capture card. I took the video signal from my HDMI monitor and sent it over to my laptop that was running Windows (same machine with Linux Mint) and the Discord call. A few settings and menus later I was installing Linux. This is where the capture broke because the HDMI signal was being funky, so we had to go to me taking a picture of the screen with my phone and then sending that to him. It worked, thankfully. 

After some navigating the menus and partitioning the SSD to fit Windows and Linux (Windows has not said a word about it), I now have Linux Mint 22.2 Cinnamon running on the desktop and I have been daily driving it since. 

It has been a challenge to get working though. Programs that I use daily are not over here yet. I am working on it though and once that is working I will make a new post about that. 

Something that I did do was skin my Linux install to look a lot like macOS. One thing about me is I LOVE the way that macOS looks and feels. It is super clean and professional looking. After doing some research and watching a video I got everything set up the way that I like it.

After doing some more things in Linux to make everything work I am pleased to announce that this is an amazing OS. A ton of projects are made by the Linux community and they have the ability to get things set up for you. The Stream Deck has several alternate apps that work with it. Focusrite is going to be a bigger challenge but it works plug and play, (with some issues). I have not tried EOS yet and I am planning on working on it. Projects like Wine and Bottles are going to be a massive help with all of this. 

![A look at my desktop](/images/minty-desktop.png)


If you are looking to get off of Windows, I recommend Linux Mint especially because it has a Windows 10 feel to it. It has been claimed to be the best beginners intro to Linux. 