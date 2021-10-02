# The NovaSonica Bundle
This bundle is a selection of effects I've made over the years to make my own music production process easier. The tools can be roughly divided into three groups: EFX, Mixing Tools and Mastering Tools. All effects have a scalable user interface and most parameters can be automated. 
  
## What's In This?
### EFX
#### Sonic Crow (ns_scr) v1.0.2  
*Dedicated to a little crow that left the world too early.*  

Probably the effect of this bundle that is the hardest to describe.  
In very technical terms: it makes a copy of your input and mixes it with the input after the amount of milliseconds you set. You can define how much the signal is shifted between the left and right channel and add *edge* to it which manipulates the delayed signal based on the current input.  
In less technical terms: it makes weird effects by messing around with a very short delay superimposed on the input signal - just give it a shot and you'll get a better idea than I can describe.   

#### Sonic Delay Sphere (ns_sds) v1.0.2  
A BPM-driven delay that makes use of stereo effects and allows you to blend forward and reverse delays using an XY-pad. 

### Mixing
#### Sonic Stereo Mixer (ns_stm) v1.0.0
This plugin is made to mix a stereo signal. Besides the usual features there are a some extras for more fine-grained control over your mix. 

##### Features

###### Volume
It's a mixer, so volume is about the minimum of control you'd expect, right? Well, this mixer supports it too.

###### Panning
A stereo mixer obviously needs to have a panning function. But, there's balance and panning which are NOT the same thing. Usually for a stereo source you would use balance and for two mono sources (panned hard left and hard right) you would use panning. For your convenience you can switch between those two modes to suit your needs. By default the balance mode is used.

###### Width
Signal too wide? Just reduce the width. Or increase it if it's too narrow. This can be very useful to make the signal stand out in your mix.

###### Phase Rotation
This is useful when you have overlapping signals like a bass guitar and a kick drum. There are multiple ways to solve the issue: EQing, sidechaining and phase shifting. The latter can be applied using this knob. Usually a minute shift of the phase is all it takes. Obviously you can also use this to achieve special effects.

###### LF:HF Balance
Your signal sounds too boomy? Turn the knob to the right. Your signal sounds too flat? Turn the knob to the left.
Under the hood this uses an LR4 crossover which is often used in speakers to split the signal into low-end and high-end signals. With the knob you control how much low-end and high-end is mixed together. By default the mix is 50/50 which means no modification of the original input. 

###### Limiter
This will ensure that your signal never exceeds -0.01dB in order to avoid clipping. Besides that it will also remove infrasound content (frequencies below 20Hz) by moving those frequencies into the audible low-end which ensures that you don't loose low-end punch while increasing the clarity of your signal. This is enabled by default.

###### Input Mode
Sometimes one needs to transform the input before mixing it. You can use any of the following input transforms:
- Stereo: the signal is not transformed
- Inverse: swaps the left and right channel
- Mix: mixes the left and right channel together
- Left: only uses the left channel of the input
- Right: only uses the right channel of the input

###### MIDI Out
Sometimes it can be really useful to use the amplitude envelope of a signal to manipulate effect parameters. If enabled this feature will use two sliders to output the signal envelopes (left and right) and send MIDI CCs for each channel. It uses CC #90 for the left channel and CC #91 for the right channel. This way you can either link the sliders to parameters of other effects or use the MIDI output to control effect parameters. By default this feature is turned off.

##### Automation
Every feature has its own slider that can be used for automation. Especially useful if you use MIDI equipment with encoders to record automation. Unfortunately REAPER doesn't allow to link MIDI encoders to the volume, panning and width envelopes. With this plugin you can work around that limitation. 


#### Sonic Auto Pan (ns_sap) v1.0.1
The name says it, it tries to automatically pan your signal. 

#### Sonic Phase Control (ns_spc) v1.0.1  
Being able to control the phase of a signal allows you to create a wide range of effects but it also enables you to employ some simple mixing tricks. For example: a kick and a bass guitar often overlap in the low end, so you have to do extra EQing to keep them separated. With Phase Control you can achieve the same without EQing by rotating the phase a few degrees, sometimes it doesn't need more than one degree to have bass guitar and kick neatly separated.  
The rotation is controlled via an XY-pad that allows you to mix the `sine` and `cosine` components of a phase rotation any way you like it. The cleanest sound is achieved if both components are represented equally, shifting them will add a different character to your signal. Besides rotating the phase you can also invert it, again controlled via an XY-pad. The inversion can be anything from 0% to 100%, left and right channel are treated independently.

#### Sonic Stereo Control (ns_ssc) v1.0.1  
This allows you to pan and mix your input signal with either the mid or the side signal which allows a wide range of manipulation for your stereo field. Useful for spatial effects, mix separation and audio restoration. 

#### Sonic Stereo Polish (ns_ssm) v1.0.1  
Wanna mess with your stereo signal? Well, here you go. This can be useful to widen a signal, or to add some noise to it, or to do both at once. Primarily it's meant to be used sparingly to enhance the stereo field, but no-one stops you from going wild with that.

### Mastering
#### Sonic Signal Meter (ns_ssm) v1.0.0  
Admit it, sometimes you just want to know what your audio looks like, right? Well, I do because that helps me to hone in on problems and it looks cool, too. This plugin is the third generation of my AudioAnalyzers ([v1](https://stash.reaper.fm/v/28703/NovaSonica%20-%20SonicAnalyzer%20-%202016-10-23.rar), [v2](https://stash.reaper.fm/v/16173/NovaSonica%20AudioAnalzer.rar)). I've rebuild all components to be scalable and make as much use as possible of the available space. As such you can scale it to a small size where it will only show a spectrum, the history of phase, left and right signal, and a goniometer. But scale it up and it will also display a spectrogram. If you hover your mouse over the spectrum and spectrogram you can see some information about that spot like frequency, tone name and current volume. If you click and keep your mouse button pressed it will show you markers for overtones which you can, for example, use to find dominant frequencies / tones. 

#### Sonic Boom Control (ns_sbc) v1.0.3
Uses a couple of tricks to allow you to boost a signal by quite a bit without applying actual compression. It does use a very little to limit the output to -0.1 dB, but not for the actual boosting. With an XY-pad you can control the sonic character and balance the high and low end of your signal. Besides that the Boom Control shifts infrasound ranges of the input into the audible low end which increases clarity without losing low end punch (a side effect that can occur when simply removing the infrasound frequencies). Untested, but this might be very useful for vinyl mastering. 

#### Sonic Limiter (ns_slm) v1.0.0
This is a simple version of the Sonic Boom Control, for when you need less control and less visual cutter. With an XY-pad you can control the sonic character and balance the high and low end of your signal. And one slider lets you control how boomy your signal sounds. Besides that the Boom Control shifts infrasound ranges of the input into the audible low end which increases clarity without losing low end punch (a side effect that can occur when simply removing the infrasound frequencies). Untested, but this might be very useful for vinyl mastering. 

#### Sonic Clean (ns_sc) v1.0.1  
This removes infrasound (< 20 Hz) and ultrasound (> 20 kHz) from your signal. Unless you want to make your listeners feel unwell there is no reason to keep these frequencies, filtering them increases clarity and reduces problems that appear when playing your audio through different stereo sets.

### Hardware Control
#### Sonic Beatstep Sequencer Controller (ns_sbsc) v1.0.0.0
This is a plugin to control the sequencer section of an Arturia Beatstep. You can enable/disable each step, set its base note and transpose it up or down. Furthermore you can set the scale, overall transpose, the swing setting and the gate setting. MIDI input to the plugin strips note-on events and uses their note values to transpose the sequence and transmits the step volume as CC #7. All other MIDI input is mapped to the MIDI channel selected and sent through without further modification. 

#### Sonic MPD218 Control (ns_smpd218) v1.0.0
This is a simple plugin to control the Full Level and Note Repeat buttons of an AKAI MPD218 unit. 

## How To Install
In REAPER open the `Options` menu and select `Show REAPER resource path in explorer/finder...`. This will open the directory where your REAPER installation lives. Open the directory `Effects` and drop the effects in there. It is a good idea to keep them in directories like in the repo, so you can install different versions and use them side by side in case of changes that break backwards compatibility. 

## Technical Background (for my fellow nerds)
Because it became tedious work to make nice UIs for the effects (as there are **no** components like buttons or checkboxes or ...) I decided to design my own version of REAPER's JSFX language, simply called **JSFX-E**(xtended). I've added support for libraries and objects, project configuration via JSON files and a grid-based UI framework for UIs that can scale to any resolution without changes to the code or complex calculations.  
  
Everything I've added to the language is designed to work well with the syntax highlighting of the [Sublime Text 3 plugin ReaSyntax](https://packagecontrol.io/packages/ReaSyntax) and code folding, some parts of it will look like standard JSFX and others may look weird at first sight, especially in the `@gfx` section.  
  
Obviously REAPER does not understand these extensions, so I also made a compiler that generates a single file with JSFX code per effect. All the code you see in this repo is generated and the original project source files are typically about 1000 lines shorter. During compilation a lot of short hands will be expanded to JSFX syntax (typical regular expression work), objects will be generated, and the UI definition will be parsed. At the end of the process the compiler tries to remove all unused functions to reduce the code size. In some cases there will be leftovers, though. These are from static classes that are referenced by libraries but never used. Since the functions in question are never called it's not an issue for the performance, but if you read the code you might stumble upon a few things that are unused.  
