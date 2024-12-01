# Volca Bass Oscillator instructions

Introducing... the “Volca Bass” Oscillator for Korg Nutekt NTS-1, by Tweeeeeak (https://www.youtube.com/channel/UC0-jZZfn5DIsHm-KicdFRkw).

This Oscillator is free. Download links:
- NTS1 original: https://github.com/tweeeeeak/nts/blob/master/a_free_osc_vbass.ntkdigunit
- NTS1 mk II: https://github.com/tweeeeeak/nts/releases/download/ntsmk2.1.0.0/vbass.nts1mkiiunit

Introduction and walk-through video: https://youtu.be/wE8cbGawHDo

Copying the “architecture” of the oscillator section of the Volca Bass, includes 3 oscillators, each with on/off, saw/square waveform, and pitch control up to +/-1 octave. Includes also a slide function, octave selection (even with the ribbon), and a step sequencer (a whaaa?!) Yes, a step sequencer, with 16 steps for notes or rest, and slide selection per step. It features 3 memory slots for sequences, and a 4th group slot, that plays all the other 3 at the same time, each to its oscillator. 

To understand how it works you really need to read the following instructions, or watch the complete video on youtube.

### Detailed instructions:

The 8 parameters of the OSCillator work as follows:

SHAPE parameter: controls the shape of the 3 OSCs: at the lowest value, all 3 OSCs are SAWs. When you turn it up, the first OSC becomes a SQUARE, then the second one, then the third one, so at the highest value all 3 OSCs are SQUAREs. This does not include all the combinations for a matter of simplicity only. For instance, it’s not possible to have OSC1 as a SAW and OSC2 as a SQUARE. To have this it would have to work as the following parameter, and it gets quite confusing as you’ll see. I didn’t see the need to allow all combinations here, but if you think it should have all combinations please let me know.

ALT parameter: controls the on/off (unmute/mute) for the 3 OSCs. From the lowest value to the highest value (and remember that you cannot see any values in the LED display here, it just shows ALT, just like the shape parameter only shows SHPE), as you turn the knob up you will pass through the following combinations of Oscillators On (O) or mute (m), for oscillator 1/2/3:
O/m/m
O/O/m
O/O/O
m/O/O
O/m/O
m/m/O
m/O/m

Edit parameter 1, 2 and 3: pitch control for OSC 1, 2 and 3, respectively. The control here is the same as the Volca Bass: from 0 upwards, each unit increments 1 cent of a tone, until 50. When it reaches 50 you will have half tone pitch up. From there upwards until 61, each unit increments half tone, until 61 which equals a full octave up. The same works downwards, from 0 to -61.

Edit parameter 4: octave and slide. This one is tricky because it controls 2 things: octave and slide. Originally it only controlled slide on/off, but with need of selecting octaves for the ribbon, I had to added it here, because it was the best parameter to do so. So, that said, it works in the range 0-21 as follows:
- 0 -- no octave, no slide. Slide is off, and the notes played are the ones on the middle octave.
- 1 to 9 -- no slide, octave 1 to 9. Means that the notes played in the ribbon are played in the selected octave. Octave 5 is the original octave, so value 5 has basically the same effect as 0.
- 10 to 19 -- same as 0 to 9, but slide is on, meaning that each time you play a new note, a slide effect is added in the first fraction of second.
- 20 -- equal to 0: no octave, no slide
- 21 -- equal to 10: no octave, slide is on

Edit parameter 5: Mode selection for sequencer (off, play, record, step record). Values 0-17. This works as follows:
- Value 0 -- sequencer is off, notes played are played in the synth normally.
- Value 17 -- record mode. To start recording: turn this parameter to value 17. Then play 16 notes, those will be recorded in the slot previously selected (see parameter 6).
- Once you record 16 notes, it will automatically enter play mode.
- If you turn it to 0, and then to 17 again, it will enter record mode again, starting at step 1.
- If you turn it to 0, and then to any value between 1 and 16, it will enter play mode.
- In play mode, when you play the synth on the ribbon, all notes played are “ignored” and the notes of the selected sequencer will be played. So all you have to do is turn the ARP on, Latch on, and it will play the sequencer.

Edit parameter 6: Slot selection for sequencer (1-4). If sequencer is off, has no effect. If sequencer is recording, values 1 to 3 select the slot for recording, and value 4 has no effect. If sequencer is playing, values 1 to 3 select the sequencer to play, and plays all OSCs at the same time (as when playing the synth with sequencer off). Value 4 plays slots 1 to 3 at the same time, each with its OSC.

Step record: Once in record mode you can turn it to any value between 1 and 16 (for instance 5) and the next note you’ll play will overwrite step 5. If you keep playing, it will continue recording steps 6, 7, etc.
If you want to “prematurely” end recording, just turn the knob to 0, and what was recorded stays there.
Check the video for details (08:54)

Recording rests: there are two ways to record a rest:
1. Record notes step by step, and the steps you don’t record will be rests
2. Long press any note for more than one second, and it will record a rest (instead of that note)

Recording slide: while recording, you can turn parameter 4 to select octave and slide. Whatever is selected when you play the note you’re recording, that is what is recorded (octave and slide on or off).

Hope this is not too confusing, but it was the simplest way I could think of for this. Let me know if it works for you , or if you have any suggestions to do it differently.

A few extra notes:
- When initiating the OSC, all parameters are set to the lowest value, so all 3 OSCs will be at -1 octave pitch.
- Shape LFO has no effect.

Please let me know what you think and give any suggestions you like.

Enjoy!

(Follow me on twitter: https://twitter.com/tweeeeeak )




