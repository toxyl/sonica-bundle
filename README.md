# The NovaSonica Bundle

## Sonic ...

### ... Auto Pan (ns_sap)
**Version**: 1.0.1  

The name says it, it tries to automatically pan your signal. 

### ... Boom Control (ns_sbc)
**Version**: 1.0.3  

Uses a couple of tricks to allow you to boost a signal by quite a bit without applying actual compression. It does use a very little to limit the output to -0.1 dB, but not for the actual boosting. Via an XY-pad you can control the sonic character and balance the high and low end of your signal.

### ... Clean (ns_sc)
**Version**: 1.0.1  

This removes infrasound (< 20 Hz) and ultrasound (> 20 kHz) from your signal. Unless you want to make your listeners feel unwell there is no reason to keep these frequencies, filtering them increases clarity and reduces problems that appear when playing your audio through different stereo sets.

### ... Crow (ns_scr)
**Version**: 1.0.2  

Dedicated to a little crow that left the world too early.  
Probably the effect of this bundle that is the hardest to describe. In very technical terms: it makes a copy of your input and mixes it with the input after the amount of milliseconds you set. You can define how much the signal is shifted between the left and right channel and add *edge* to it which manipulates the delayed signal based on the current input. In less technical terms: it makes weird effects by messing around with a very short delay superimposed on the input signal - just give it a shot and you'll get a better idea than I can describe.   

### ... Delay Sphere (ns_sds)
**Version**: 1.0.2  

A BPM-driven delay that makes use of stereo effects and allows you to blend forward and reverse delays using an XY-pad. 

### ... Phase Control (ns_spc)
**Version**: 1.0.1  

Being able to control the phase of a signal allows you to create a wide range of effects but it also enables you to employ some simple mixing tricks. For example: a kick and a bass guitar often overlap in the low end, so you have to do extra EQing to keep them separated. With Phase Control you can achieve the same without EQing by rotating the phase a few degrees, sometimes it doesn't need more than one degree to have bass guitar and kick neatly separated.

### ... Stereo Control (ns_ssc)
**Version**: 1.0.1  

This allows you to pan and mix your input signal with either the mid or the side signal which allows a wide range of manipulation for your stereo field. Useful for spatial effects, mix separation and audio restoration. 

### ... Signal Meter (ns_ssm)
**Version**: 1.0.0  

Admit it, sometimes you just want to know what your audio looks like, right? Well, I do because that helps me to hone in on problems and it looks cool, too. This plugin is the third generation of my AudioAnalyzers ([v1](https://stash.reaper.fm/v/28703/NovaSonica%20-%20SonicAnalyzer%20-%202016-10-23.rar), [v2](https://stash.reaper.fm/v/16173/NovaSonica%20AudioAnalzer.rar)). I've rebuild all components to be scalable and make as much as possible of the available space. As such you can scale it to a small size where it will only show a spectrum, the history of phase, left and right signal, and a goniometer. But scale it up and it will also display a spectrogram. Hovering over the spectrum and spectrograph you can see some information about that spot like frequency, tone name and current volume. If you keep you mouse pressed it will show you markers for overtones which you can, for example, use to find dominant frequencies / tones. 

### ... Stereo Polish (ns_ssm)
**Version**: 1.0.1  

Wanna mess with your stereo signal? Well, here you go. This can be useful to widen a signal, or to add some noise to it, or to do both at once.
