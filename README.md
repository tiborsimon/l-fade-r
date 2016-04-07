# L Fade R

<a title="Latest version" href="https://github.com/tiborsimon/l-fade-r/releases/latest" target="_blank">
   <img src="https://img.shields.io/badge/version-v1.0--beta.0-green.svg?style=flat" />
</a>
[![Gitter](https://badges.gitter.im/tiborsimon/l-fade-r.svg)](https://gitter.im/tiborsimon/l-fade-r?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
<a title="License" href="#license">
   <img src="http://img.shields.io/badge/license-MIT-lightgray.svg?style=flat" />
</a>

Real-time spatial audio filter with [Pure Data](http://puredata.info). 
Discover your favorite records in a whole new perspective. You can interactively fade between the __left__ and __right__ 
channels, and __L Fade R__ will mix the modified mix into a single __mono__ channel.

I created this simple audio tool for _practicing_ the guitar and for _discovering_ my favorite records in a new perspective. I am a 
guitar player, and I like to practice my favorite songs while I listen to the music itself. With __L Fade R__ I am be able to 
filter out the main guitar parts from most of the records I listen to _without any quality loss_. The actual result depends on the mix. __L Fade R__ is mainly useful for guitar players, as the guitar is the instrument that often mixed in one side of the record.

<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/l-fade-r-gui.png" alt="L Fade R GUI" width=178 />

__L Fade R__ is also suitable for discovering your favorite music in a new level. By listening only one panoramic side of the record, you will be able to hear unheard melodies. If you hear discover something new, don't forget to share it with others. There is a dedicated [#l-fade-r]() hashtag on Twitter for this purpose.

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
(2015.04.01) available release (0.46.7) for Windows and OS X and they worked fine for me. I used the _vanilla_ release because it is a much smaller package than the feature packed _extended_ release.

Follow this link to download your copy of __Pure Data__: http://puredata.info/downloads

# Routing your system audio to Pure Data

To process your system sound with __Pure Data__, you need to route your system audio to it first. For this purpose I 
use [Virtual Cable]() on Windows and [Soundflower]() on OS X. There are alternative solutions also.

## Setting up Virtual Cable on Windows

Download and install the latest __Virtual Cable__ from it's official website: http://vb-audio.pagesperso-orange.fr/Cable/

After you installed __Virtula Cable__ on your machine, you have to go to the _Control Panel_ -> _Sound_ settings, and select _CABLE Input_ as your playback device. Then in Pure Data go to _Media_ -> _Audio Settings_ and choose _CABLE Output_ as the input. It is a good idea to turn off any sound enchancement as it can mix the left and right channels together, and you can't achieve a full left-right separation.

<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/win-settings-01.png" alt="L Fade R GUI" width=178 />
<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/win-settings-02.png" alt="L Fade R GUI" width=178 />
<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/win-settings-03.png" alt="L Fade R GUI" width=178 />

## Setting up Soundflower on OSX

Download and install the latest __Soundflower__ release from GitHub: https://github.com/mattingalls/Soundflower

After you installed __Soundflower__ on your machine, you have to go to the _System Preferences_ -> _Sound_ settings, and select _Soundflower (2ch)_ as your output. Then in Pure Data go to _Media_ -> _Audio Settings_ and choose _Soundflower (2ch)_ as your input.

<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/osx-settings-01.png" alt="L Fade R GUI" width=178 />
<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/osx-settings-02.png" alt="L Fade R GUI" width=178 />

# Using L Fade R

If you completed the previous configuration part on your machine, you are ready to use __L Fade R__. There are 3 pure data files in the package:

| File name | Purpose |
|:----------|:--------|
| `l-fade-r.pd` | The main __L Fade R__ file you should use. This file uses the other two files (core and the docs)<br />to provide a clean and simplified interface. |
| `l-fade-r-core.pd` | This file contains the core DSP functionality of __L Fade R__. You can use this file instead of<br /> `l-fade-r.pd` if you want to see the internal workings during operation. |
| `l-fade-r-docs.pd` | Common user manual file. You should not use it, as it is used by the other two files. |

To use __L Fade R__ you:

1. Open up `l-fade-r.pd` or `l-fade-r-core.pd`
2. Make sure you redirected your system sound and you are using that redirected source as input in _Media -> Audio Settings_.
3. Turn on DSP (in the main window or in __L Fade R__ with the toggle switch (_DSP_on/off_).
4. You are ready to go.
5. Adjust the fade with the top, horizontal slider, and adjust the volume with the bottom, vertical slider.
6. Optionally you can test your setup with the _Test_ toggle switch. You should hear a low pitch sine signal in the left cahnnel and a hight pitch sine signal in the right channel.

<img src="https://raw.githubusercontent.com/tiborsimon/l-fade-r/master/docs/l-fade-r-gui.png" alt="L Fade R GUI" width=178 />

You can bypass __L Fade R__ at any time with the _Bypass_ toggle switch.

# Contribute

There is a [Wiki page](https://github.com/tiborsimon/l-fade-r/wiki) where I started to collect the records I processed with __L Fade R__. There is information about what you will hear by fading left or right with __L Fade R__. This could be useful, if you want to practice a special part, and want to see if that part could be filtered out with __L Fade R__.

I also used a rating of 5 levels. 5 means that the record is very good for practicing (GP = Guitar Practicing), 1 means it is not the best record to separate parts out.

You can contribute to this [Wiki page](https://github.com/tiborsimon/l-fade-r/wiki) if you want. Make sure follow the contributing guide at the top of that [Wiki page](https://github.com/tiborsimon/l-fade-r/wiki).

# License

__L Fade R__ in under the __MIT License__.

Copyright (c) 2016 Tibor Simon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

