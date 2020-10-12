---
layout: default
title: Tools
permalink: /tools/
tags: tools
---

# What do I use?

## hardware

A collection of tools that I use.

- Computer: MacBook Pro (2020, 13-inch)
- Mobile: iPhone X, iPad Pro (2020, 12.9-inch)
- Mouse: Logitech MX Master 3
- Camera: Nikon F5, 50 mm f/1.4 AF-D
- Scope: HP 54600A (DSO)

## software
*Note: I use a MacBook and an iPhone, and a sexy Linux machine for compute.*

### Computer software

#### Utilities

- [Magnet](https://magnet.crowdcafe.com/index.html) to resize and snap windows
  to a grid. Makes multitasking a charm, and is surprisingly not natively
  implemented on Mac OS.
- [Alfred](https://www.alfredapp.com) as a smart replacement to Spotlight.
- [InsomniaX](https://github.com/semaja2/InsomniaX) to keep my laptop from going
  to sleep when I'm presenting or reading. Now that it has stopped being actively
  developed, I now recommend [Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12) instead.
- [NetNewsWire](https://ranchero.com/netnewswire/) is a great free and open
  source RSS reader for Mac and iOS.
- [Pocket](https://getpocket.com/premium) for queueing up articles to read later
  instead of reading everything right now. I prefer the look and feel of
  Instapaper, but stopped using it since they made full-text search a premium feature.
  I'm planning to self-host [Wallabag](https://www.wallabag.org/en) on my server
  as soon as I have the time. 
- [Dropbox](https://dropbox.com) is indispensible for backups, cloud storage and sharing.

 
### Phone apps

- I bought an iPad Pro because I was bored in quarantine. Little would I know, it
  has paid tremendous dividends.
  - 12.9-inch because the 11-inch keyboard would be too small for any
    substantial amount of typing. Besides, screen real-estate is very important
    when writing notes and annotating PDFs. Portability is no issue, it can fit
    on your lap, in your tote bag and the tray table of an airplane.
  - I use it to carry around a small library of interesting books, papers and
    articles. It feels amazing to have everything I need in one device.
  - It's an amazing device to write stuff on.
  - 

#### Contact tracing

First, download the SingPass app. It's fast, convenient, and promises not to spy
on you (hopefully!).

Then [configure your iPhone][safe-entry] to make SafeEntry a more pleasant experience on iOS.
It should save some taps and time futzing around with a camera in front of QR codes
at entrances and exits. Kudos to mrbrown for posting about this.

1. Go to the SingPass app to activate Siri Shortcuts for SafeEntry.
1. Go to Settings ➡️  Accessibility ➡️  Touch ➡️  Back Tap, and turn it on.
1. Assign Scan SafeEntry to Double Tap, and SafeEntry Check-out to Triple Tap.
1. You can now double-tap the back of your iPhone to activate SafeEntry and
   triple-tap to check out.

Note: the Back Tap feature only works for iPhone 8 and above.

## bookmarklets

Instead of installing browser extensions which slow down startup time and
constantly chew up resources, bookmarklets are efficient for simple tasks. Each
of these links is a little [snippet of
JavaScript](https://www.mattcutts.com/blog/javascript-bookmarklet-basics/) which
you can bookmark.

- [Autoscroll][autoscroll] when reading a longform text while keeping your hands
  free. Esc to stop scrolling, -/+ to speed up and slow down.


[safe-entry]: https://www.facebook.com/mrbrownlah/posts/3263850646998130
[autoscroll]: javascript:/*The%20Autoscroll%20Bookmarket:Tim%20Harper:http://tim.theenchanter.com*/var%20_ss_interval_pointer;_ss_speed=1;_ss_speed_pairs=%5B%5B0,0%5D,%5B1,200.0%5D,%5B1,120.0%5D,%5B1,72.0%5D,%5B1,43.2%5D,%5B1,25.9%5D,%5B2,31.0%5D,%5B4,37.2%5D,%5B8,44.8%5D,%5B8,26.4%5D,%5B16,32.0%5D%5D;_ss_last_onkeypress%20=%20document.onkeypress;_ss_stop=function()%7BclearTimeout(_ss_interval_pointer)%7D;_ss_start=function()%7B_ss_abs_speed=Math.abs(_ss_speed);_ss_direction=_ss_speed/_ss_abs_speed;_ss_speed_pair=_ss_speed_pairs%5B_ss_abs_speed%5D;_ss_interval_pointer=setInterval(%27scrollBy(0,%27+_ss_direction*_ss_speed_pair%5B0%5D+%27);%20if((pageYOffset%3c=1)%7C%7C(pageYOffset==document.height-innerHeight))%20_ss_speed=0;%27,_ss_speed_pair%5B1%5D);%7D;_ss_adj=function(q)%7B_ss_speed+=q;if(Math.abs(_ss_speed)%3e=_ss_speed_pairs.length)_ss_speed=(_ss_speed_pairs.length-1)*(_ss_speed/Math.abs(_ss_speed))%7D;_ss_quit=function()%7B_ss_stop();document.onkeypress=_ss_last_onkeypress;%7D;document.onkeypress=function(e)%7Bif((e.charCode==113)%7C%7C(e.keyCode==27))%7B_ss_quit();return;%7D;if(e.charCode%3e=48&&e.charCode%3c=57)_ss_speed=e.charCode-48;else%20switch(e.charCode)%7Bcase%2095:_ss_adj(-2);case%2045:_ss_adj(-1);break;case%2043:_ss_adj(2);case%2061:_ss_adj(1);break;%7D;_ss_stop();_ss_start();%7D;_ss_stop();_ss_start();

