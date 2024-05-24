## Proba-B Oscillator instructions

Introducing Proba-B, probability sequencer oscillator for Korg NTS-1, by Tweeeeeak (https://www.youtube.com/channel/UC0-jZZfn5DIsHm-KicdFRkw).

Twitter: https://twitter.com/tweeeeeak

This Oscillator is free. Download link:
https://github.com/tweeeeeak/nts/releases/download/2.0.0/proba-b_v210.ntkdigunit

Introduction and walk-through video: https://youtu.be/CADbPm17Uhw

Quick reference sheet (a must to be able to work with the multiple parameters this oscillator offers):
[Proba-b.2.10.Reference.Sheet.pdf](https://github.com/tweeeeeak/nts/releases/download/proba-b.2.0/Proba-b.2.10.Reference.Sheet.pdf)

### Release notes:

**Version 2.1** includes the following additional feature (search [Version 2.1] on this manual to see them in detail):
- Function 11 - Microtuning: set microtuning for each note, either as a scale mode, or for any note in any octave

**Version 2.0** includes the following additional features (search [Version 2] on this manual to see them in detail):
- Function 8 – Randomize probability values
- Function 9 – Freeze sequence (Repeat the last generated sequence over and over again)
- Function 10 – Edit sequence begin and end steps with SHAPE and ALT parameters 
- Drone mode (param 4 value 22) - use when you set NTS-1 envelope to OPEN
- Step record now doesn't advance automatically when you record a step, to cope with the NTS-1 ribbon instability

### Description

Proba-B is a sequencer based oscillator. Use the built-in arpeggiator or record a step sequence, from 1 to 64 steps (default is 8 steps).
Then assign probability values to each step, for step mute, transpose and shape change.
The oscillator waveshape itself is a triangle waveform, with wave folding (shape parameter) and frequency modulation (alt parameter).

Works great with delay effects.

Extra features include: time division and transpose, with auto minor to major scale converter.

It can become quite complicated, but remember that you can simply start by using the arpeggiator, and start setting some probability values for each step.

To understand how it works you really need to read the following instructions, or watch the complete video on youtube. Don't forget to use the quick reference sheet as well.

Here’s how it works in detail:

### SHAPE parameter

By default changes wave folding amount

### ALT parameter

Changes frequency modulation amount. The modulator shape and frequency is the same as the main oscillator (carrier). When it reaches halfway it starts changing frequency to an octave lower, and after 3/4 starts changing to 2 octaves lower.

### OSC PARAM 1 – Mute probability

The parameter value chooses the step, then using the SHAPE parameter affects the probability to mute that particular step.

### OSC PARAM 2 – Octave transpose probability

The parameter value chooses the step, then using the SHAPE parameter affects the probability to transpose that particular step by up to +/- 2 octaves.

### OSC PARAM 3 – Shape change probability

The parameter value chooses the step, then using the SHAPE parameter affects the probability to change the shape of the waveform on that particular step. The amount of shape change is also randomized, and affects both wave folding and frequency modulation.

Note: Turn either parameter 1, 2 or 3 to value 0, and SHAPE parameter will now change wave folding amount again.

### OSC PARAM 4 – Octave and slide

This one is tricky because it controls 2 things: octave and slide. It works in the range 0-21 as follows:
- 0 -- no octave, no slide. Slide is off, and the notes played are the ones on the middle octave.
- 1 to 9 -- no slide, octave 1 to 9. Means that the notes played in the ribbon are played in the selected octave. Octave 5 is the original octave, so value 5 has basically the same effect as 0.
- 10 to 19 -- same as 0 to 9, but slide is on, meaning that each time you play a new note, a slide effect is added in the first fraction of second.
- 20 -- equal to 0: no octave, no slide
- 21 -- equal to 10: no octave, slide is on
[Version 2]
- 22 -- equal to 0: no octave, no slide. Drone mode on. Use drone mode when you set the Envelope to OPEN, or with a long Release (bigger release then step time). It will work better by continuing to release on the next step if the next step is muted, avoiding abrupt silences that create clicks that are specially anoying when you add delay or reverb effects.

## OSC PARAM 5 – Sequencer Mode or Function value

By default, it sets the Sequencer Mode that allows to record or play the sequencer, or turn it off. Values 0-65. This works as follows:
- Value 0 -- sequencer is off, notes played are played in the synth normally.
- Value 65 -- record mode. To start recording: turn this parameter to value 65. Then play 8 notes (or the number of steps previously defined for the sequencer), those will be recorded on the sequencer.
- Once you record all notes, it will automatically enter play mode.
- If you turn it to 0, and then to 65 again, it will enter record mode again, starting at step 1.
- If you turn it to 0, and then to any value between 1 and 64, it will enter play mode at step 1.
- In play mode, when you play the synth on the ribbon, all notes played are “ignored” and the notes of the selected sequencer will be played. So all you have to do is turn the ARP on, Latch on, and it will play the sequencer.

**Step record**: Once in record mode you can turn it to any value between 1 and 64 (for instance 5) and the next note you’ll play will overwrite step 5. If you keep playing, it will continue recording steps 6, 7, etc.

[Version 2] Since version 2 of Proba-B, if you start step record, the sequence no longer advances automatically to record next step. In the example above, if you select value 5, and keep playing several notes, you will be overwriting step 5, until you turn the knob to other value. This is done to cope with the instability of the NTS-1 ribbon, so it is easier to record a sequence.

If you want to “prematurely” end recording, just turn the knob to 0, and what was recorded stays there.

Check the video for details (13:29)

**Recording rests**: there are two ways to record a rest:
1. Record notes step by step, and the steps you don’t record will be rests
2. Long press any note for more than one second, and it will record a rest (instead of that note)

**Recording slide**: while recording, you can turn parameter 4 to select octave and slide. Whatever is selected when you play the note you’re recording, that is what is recorded (octave and slide on or off).

### OSC PARAM 6 – Function select

This parameter selects a function (setting), and then you can use OSC PARAM 5 to set that function value. Here’s the list of functions:

1 – Sequencer mode: PARAM 5 works as sequencer mode, like described above

2 – Reset step: turn PARAM 5 to any value, and as soon as you change the value, the probability sequencer is reset to step 1. This is useful when you use the arpeggiator, before you start it, to make sure that the first note you play will fit into step 1 of the probability sequencer. (Note: when using the step sequencer, it is always in sync with the probability sequencer)

3 – Step length: use PARAM 5 to select the number of steps of the step sequencer and probability sequencer (values 0 and 65 are ignored)

4 – Multi edit: if you set PARAM 5 to a value greater than 0, you will make it possible to edit the probability for multiple steps at once. For instance:
- If you set PARAM 5 to 1, when you change the Mute probability for step 1, it will change that probability for all steps in the sequence.
- If you set PARAM 5 to 3, when you change the Mute probability for step 1, it will change that probability for steps 1, 4, 7, and so on; and when you change the Mute probability for step 5, it will change that probability for steps 5, 8, 11, 14, and so on.
- If you set PARAM 5 to 0 it returns the default functionality, meaning that changing the probability for one step only affects that particular step

5 – Time division. By default is 1, but if you set a higher value (with PARAM 5), it will add that amount of mute steps between sequencer steps. For instance, value 2 results in a time division of 1/2, value 3 on 1/3, and so on. Works with the step sequencer, but can also work with the arpeggiator, but in the latter it simply mutes steps, doesn’t really really correspond to time division.

6 – Transpose On/Off: Turn PARAM 5 to any value > 0, and you activate transpose. For that to work, set the arpeggiator octave value to 1, so it plays continuously the same note. The original sequence is played if you play the first non-rest note of the recorded sequence. For instance, if your recorded sequence starts with a D on step 3 (and step 1 and 2 are rests), then playing the D note on the keyboard (with the arpeggiator working) plays the original sequence. If you play the note E on the keyboard, the sequence is transposed up by one full tone. And so on.

7 – Minor to Major scale converter On/Off. Turn PARAM 5 to any value > 0, and you activate Minor to Major scale converter while transposing. Transpose must be on. What this does is converts a minor scale note on the recorded sequence to a major scale note, if the sequence is being transposed. This is very specific to a certain music style, but it’s something that bugs me in particular. Typically when you record a sequence in a minor scale, say D minor, if you transpose it to C, you want it to become C major. It’s very difficult to have this with sequencers that allow transposing, maybe because it’s too specific. But hey, I wanted this 😊. So, if you activate this function, all transposed sequences become Major, and only the original remains Minor.

8 [Version 2] - Randomize probability values. Turn PARAM 5 to any value > 0. When you turn PARAM 5 to value 1, a few probability values will be randomized (at random steps), so a new sequence will play, which is slightly different from the original. Value 2 will change a few more probability values, and so on until 64. If you change back to value 0, the original sequence will play. Values 1 to 64 will also keep the randomized probability values, so they work as 64 slots of growing difference from the original sequence.

9 [Version 2] - Freeze sequence. Turn PARAM 5 to 0 = OFF (Unfreeze), Other = Freeze. Freeze means than the values generated by the probability sequence for each step (for mute, octave and shape change) will be repeated, instead of randomized, in each loop. The effect is that the sequence will sound the same, repeatedly.

10 [Version 2] - Begin/end step edit. Turn PARAM 5 to 0 = OFF, Other = ON. When begin/end step edit is one, SHAPE/ALT parameters will change begin/end steps, respectivelly, instead of their normal values. This is a quick way to tweak a sequence playing by simply changing the first and last step. Keep SHAPE param lower than ALT (first step lower than last step), otherwise the sequence will play only one step repeatedly.

11 [version 2.1] - Microtuning. Turn PARAM 5 to 0 = OFF, 1 = ON Full Mode, 2 or greater = ON SCALE Mode.
Then change SHAPE parameter to change microtuning for the currently playing note. If there is no note playing, the last played note will be affected.
On Full Mode, when you change microtuning for a note, in any octave, that particular note in that particular octave is affected.
On Scale Mode, when you change microtuning for a note, that note is affected on any octave. For instance, if you change D3 microtuning, for -10% of a tone, for instance, D2 will also be changed -10% of a tone. I called this the scale mode because it allows you to set different 12-note scales. 

Hope this is not too confusing. Let me know if it works for you , or if you have any suggestions to do it differently. 

A few extra notes:
- There is no full reset function, and with this multiple set of parameters, if you change to another OSC than back to Proba-B, the result is impredictable. In that case, it's best to turn the NTS-1 off and on again.
- Shape LFO affects wavefolding, a little bit (not the full scale of the parameter)

Please let me know what you think and give any suggestions you like.
You can use the comments section on youtube, or Direct Message on Twitter.

Enjoy!

(Follow me on twitter: https://twitter.com/tweeeeeak )

