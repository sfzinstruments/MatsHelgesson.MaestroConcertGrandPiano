# The Maestro Concert Grand Piano

This is a sampled reproduction of a Yamaha CF-3 grand
piano from the early 90s. It was chromatically sampled,
to maintain the tempered tuning.

Created by Mats Helgesson, 2003, originally in Gigasampler format, converted to
flac for SFZ format by kinwie and published with the permission of the author
on May 16, 2020 via e-mail.

Audio demo :
https://sfzinstruments.github.io/pianos/maestro_concert_grand_piano

See the `mcgreadme.txt` file included with this archive about other details and
legal notice.

# Technical

The Giga file is 985 mb.
Maestro Concert Grand contains 452 stereo samples.
It was recorded with a pair of Neumann KM84 microphones
in X/y stereo. x/y provides excellent mono compatibility.

The samples are sorted in 5 velocity layers, of which
velocity 0-29 are piano, 30-59 are mezzo piano, 60-89
are mezzo forte, 90-108 are forte and 109-127
fortissimo.

Maestro Concert Grand is the second sample set with pedal
up and down sounds separate from the key samples. It gives
you, the artist, the choice of adding additional pedal
noise in your recordings for added realism. They are
located in a second patch, below the piano key range, at
midi key number 12, 13, 14, 15, 16 and 17.

**note**: This is changed with Concert Grand v2, which has
separate versions of the piano, and additional release
samples in four velocities, adding 352 samples.



## Compatibility Notes

This SFZ Instrument is reconstructed with the heavily use of SFZ specification level 2.0 + ARIA Extensions. With this is mind, this instrument will only played properly in Plogue sforzando and similar sfz samplers that used ARIA Engine. Trying to play this instrument in other than ARIA-based sfz samplers may cause issues and problems if it doesn't support the opcodes superset used in this sfz instrument. If ARIA-based sfz sampler is not your choice, we advised you to choose a sfz sampler that has similar level of opcodes support for this instrument can be played and sounded as it should.

## Control Details

Pedals and Lid noises has been moved to Pedal CCs in this SFZ version.
- Sustain pedal noise, at Sustain pedal CC64
- Mid pedal noise, at Sostenuto pedal CC66
- Lid noise, at Soft pedal CC67

- Release : Release time for the sustain layers
- Rel.Noise : Key-release noise volume
- Ped.Noise : Pedals noise volume (all 3 pedals)
- Veltrack : Dynamic range / velocity to volume response

## Improvements and Features

- This piano has the note-selfmasking sfz native feature and polyphony optimized. This means, when playing a lot of notes (e.g. repetitive, trills or sustain pedal down), the voices count will be handled effectively and lower, which also means less jumping in CPU usage and results in more natural piano sound behavior.

- When not used, lowering the Rel.Noise and Ped.Noise to 0% also disabling those layers which means free up their polyphony usage and lowering voice count, so lesser CPU and RAM usage.

## Usage Tips

- Setting Veltrack value to achieve a pleasant dynamic range that suit you also depend on your playing style and your keyboard/MIDI controller touch response. Try increase and decrease this "Veltrack" parameter as you play and feel the suitable one for you. To change the default value permanently, find this line in the sfz file : `set_hdcc$VELTRACK=1` and change the value to the one you that wanted, range from 0 to 1.

- MIDI CC numbers are assigned at the top of the sfz file with the #define macro. They can be easily changed to your personal favor or to match your MIDI controller device setup. After loading the instrument in sforzando, click the "Open In Text Editor" blue botton at the INFO page, the sfz file will open by your default text editor. You will see a list of parameter's defined numbers. Change the number to your preference and then save it (e.g. Ctrl+S in WinOS), the CC numbers are updated to new ones. This is a handy feature in sfz and is a bit similar to MIDI Learn function.

- The velocity ranges can be adjusted directly also using "Open In Text Editor" button to match your taste or keyboard response. 5 velocity for sustain layers : `#define $LOVELx` /  `#define $HIVELx` and 4 velocity for release noise layers : `#define $REL_LOVELx` / `#define $REL_HIVELx`

- Try add a Mid-Side plugin after sforzando, and lowering the mid level to make this Maestro Piano more wider. Also increase some low frequency and decrease high-mid frq, by adding an EQ plugin after sforzando can add warmth to the sound.

## Update Log

- Aug 23, 2020 : Cosmetic update.

- Aug 18, 2020 : Renumbering polyphony group.

- May 30, 2020 : Use release settings from original settings instead of curve definition which cause problem when sustain pedal involved. This issue was reported by Jeff Learman.
