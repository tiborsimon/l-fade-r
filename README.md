# L Fade R

Real-time spatial audio filter with [Pure Data](http://puredata.info). 
Discover your favorite records in a whole new perspective. You can interactively fade between the __left__ and __right__ 
channels, and __L Fade R__ will mix the modified mix into a single __mono__ channel.

I created this simple audio tool for my [interactive YouTube guitar videos]() and also for practicing. I am a guitar 
player, and I like to practice to my favorite songs while I listen to the music itself. With __L Fade R__ I am be able to 
filter out the main guitar parts for most of the records (it depends on the actual mix) I listen to _without loosing quality_.

# Requirements

- [Pure data](http://puredata.info)
- Route your system audio into __Pure Data__

# Installing Pure Data

Excerpt from the official __Pure Data__ site:

>
Pure Data (aka Pd) is an open source visual programming language. Pd enables musicians, visual artists, performers, 
researchers, and developers to create software graphically, without writing lines of code. Pd is used to process and 
generate sound, video, 2D/3D graphics, and interface sensors, input devices, and MIDI.
>

You can install __Pure Data__ with the installers downloaded from it's official website. I have tested the currently 
(2015.04.01) available release (0.46.7) for Windows and OS X and they worked fine for me.

Follow this link to download your copy of __Pure Data__: http://puredata.info/downloads

# Routing your system audio to Pure Data

To process your system sound with __Pure Data__, you need to route your system audio to it first. For this purpose I 
use [Virtual Cable]() on Windows and [Soundflower]() on OS X. There are alternative solutions also.

Download and install the latest __Soundflower__ release from GitHub: https://github.com/mattingalls/Soundflower

Download and install the latest __Virtual Cable__ from it's official website: http://vb-audio.pagesperso-orange.fr/Cable/





