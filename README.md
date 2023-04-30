# Pd-Vanilla-SUBHARMONIC-SYNTH

The subharmonic synth patch I made is inspired by the Moog Sub-Harmonicon and it is a framework on which a more complete synthesizer (with GUI) can be developed.

The fist version (v1.0) is the raw draft on which I made the video on my YouTube channel in November 2021.

Version 1.2 instead (v1.2) is an improved and simplified patch version.

v1.2 updates:
1) replacement of the 16 [sel] objects below Sub1_Freq sliders with a single [sel 16..1]
2) The sub harmonic frequency computation has been drastically simplified. No more [b][b][b][b][b] ... or [sel 16][sel 15][sel 14][sel 13][sel 12] and so on.
3) The previous [s BaseFreq1] and [s updateSlider] are now merged using a [t b f].
4) Phrygian scale section was simplified and OSC1_PhrygianNote slider was replaced with a [hradio].
5) I added two green sliders to manually control the Filter Cutoff and QFactor without using an external controller.
6) Improved filter behaviour using [vcf~] insead of a cascade of [lop~] and [bp~]. No more clicking noise when changing the cutoff frequency. 
7) Extended cutoff frequency range (100 - 8200 Hz).
