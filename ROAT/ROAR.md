## RoaR Oscillator instructions

Introducing the “RoaR” Oscillator for Korg Nutekt NTS-1, by Tweeeeeak (https://www.youtube.com/@tweeeeeak228).

This Oscillator is free. __Download links__:
- NTS1 original: [roar.ntkdigunit](https://github.com/tweeeeeak/nts/releases/download/roar.1.01/roar.ntkdigunit)
- NTS1 mk II: [roar.nts1mkiiunit](https://github.com/tweeeeeak/nts/releases/download/roar.1.01/roar.nts1mkiiunit)

Youtube introduction: https://youtu.be/vCKhyWSqCxs

RoaR is an oscillator that randomly generates digital sounds and sequences, with a simple turn of a knob. Each sound can be a simple patch or a rhythmic (16 step) sequence. 

__Knob A [RAND]__ controls how complex and glitchy your sound will be. Low values generate simple, tuned and playable sounds, while high values generate more glichy, complex and total random sounds.
A simple touch on knob A generates a new sound or sequence. The best thing is to try it out. You'll see some sounds are single notes, other are running sequences. It's random!

__Knob B [PROG]__ selects 16 different random sounds, with the same level of randomization where you left knob A. However, while you don't touch knob A again, these 16 sounds will be fixed.
This means that you can be sure that you allways get the same sound at the same position of knob B. But only if you don't touch knob A, because if you move knob A again, a new set of 16 random sounds will
be generated.

### Extra parameters

_Note: you can access the Extra Parameters by long pressing the OSC button and turning the TYPE knob._

__Param 1: SYNC__ - Turn SYNC on to run the sequenced sounds only when the NTS-1 ARPeggiator or SEQuencer is running. This way the sequences are synchronized to the ARP/SEQ tempo. This way you can also synchronize the sequenced sounds to external equipment, when you sync the NTS-1 ARP that way, using the Sync in/out ports, or via MIDI.

__Param 2: BPM__ - BPM sets the tempo of the sequenced sounds, only when SYNC is OFF. (Note that on NTS1 original (mk1) this parameters is called TEMP (for tempo)
and varies between 1 and 100).

### Oscillator architecture (ROAT oscillator)

Under the hood, __RoaR__ is basically the [ROAT oscillator](ROAT.md), which itself is a recreation of the SOMA Rumble of Ancient Times synthesizer, and includes 4 oscillatores, each with 16 possible waveforms, independent detuning, LFO and rhythmic sequence, and combinable in more than 1000 ways.

You can [check it out](ROAT.md) and download (it's free) and try it out as well. It will allow you to manually change all parameters that are randomized in RoaR.

