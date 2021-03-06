# sib2humPlugin
A Sibelius plugin to convert Sibelius scores to Humdrum

Work in progress

## Version 0.14.2
* Consolidated loops in HEADER OF KERN FILE section
* Fixed small typo in gracenote code

## Version 0.14.1
* Cleaned formatting of if statements

## Version 0.14
* Initial support for grace notes. Slurs and ties for grace notes are not supported at the moment.

## Version 0.13
* Initial support for slurs
* Reopened https://github.com/hleveillegauvin/sib2humPlugin/issues/3#issue-1152645870

## Version 0.12
*  Clean exit if no active score or active score with 0 staff

## Version 0.11
* Hidden rests are now encoded using yy 

## Version 0.10.1
* Fixes https://github.com/hleveillegauvin/sib2humPlugin/issues/3#issue-1152645870
* Fixes a bug with start repeat token

## Version 0.10
* Ties are supported, but assumes at tie is resolved in same staff/same voice
* Added a TrimTabsLeading method, which simplifies the code and fixes some issues where tabs were either an extra tab was present between spines, or a tab car was missing
* humNewTimeSignatureLine and humNewMeterLine didn't take voices into consideration. Fixed.

## Version 0.09
* Keeps track of clef changes throughout the score
* Fixed an issue with the code that keeps track of new key signatures

## Version 0.08
* Tuplets are now supported, including the use of extended \*\*recip representation when needed. (I think this works, but more QA on this would be great, as math is not my forte) 

## Version 0.07
* Supports multiple voices
* Progress bar added

## Version 0.06
* Articulations and fermatas are now supported
* Minor modifications to ConvertPitch method

## Version 0.05
* Spines are now in the correct (i.e. reverse from Sibelius) order
* Fixed an issue with Whole-Measure Rests. Still uses "rr" though.

## Version 0.04
* Dictionaries for pitches and accidentals. Supports up-to double flats/sharps. Other type of accidentals (e.g. quarter tones) not supported.
* Following C.Sapp's changes to Instrument Code, \*Iud   => \*Ioud

## Version 0.03

* Dictionaries for durations (tuplets are ignored for now), supports Whole-Measure Rests, but with generic "rr", not the more elegant x%yr version.
* All pitches are assigned to C right now, for QA'ing in Verovio
* Chords are taken into considerations, but not voices (assume always voice 1 for now).
* Fixes an issue with retrieving NoteRests that was present in past version.

## Version 0.02

* Keeps tracks of new key signatures and new time signatures (but assumes all staves have same key and same time signature)

## Version 0.01

 * Generates a legal Humdrum file.
 * Retrieves Score info and correctly converts to Humdrum format
 * Dictionaries for clefs, key signatures, time signatures (including c and c| time)
 * Dictionnary for ~ half the possible instruments in Sibelius. Unmapped instruments appear as \*I?? for the moment
 * Long and short names of instruments are recorded properly
 * Barlines with bar numbers are at correct position
 * Basic syntax to evaluate events vs null token is in place (at the moment, events are all marked as X)

----------------------------------------------------

ToDo

**Must Have**
- [ ] Articulations
- [ ] Dynamics + Crescendi
- [ ] Pickup bar(s)
- [ ] Tempo markings
- [ ] Make sure that the file generated doesn't have an extra return carriage character at the end.
- [ ] first and second endings

**Should Have**
- [ ] Verify instrument changes througout the Score (currenrtly only initial _ is recorded)
- [ ] Support slurs for more complex cases
- [ ] Ties and slurs for grace notes
- [ ] More instruments supported

**Nice to Have**
- [ ] Add support for multistaff instrument (e.g. piano) \*staff2	\*staff1 
- [ ] Beaming (although not urgent; Verovio can do it automatically)
- [ ] Create GUI for users to define Custom1Artic, Custom2Artic and Custom3Artic and assign them to undefined signifiers
- [ ] Create GUI to decide name of file and where to save (is this feasible? Can't find an example of an existing plugin that lets you do that)
- [ ] Piano pedal indications
