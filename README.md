# sib2humPlugin
A Sibelius plugin to convert Sibelius scores to Humdrum

Work in progress

## Version 0.03

* Dictionaries for durations (tuplets are ignored for now), supports Whole-Measure Rests, but with generic "rr", not the more elegant x%yr version.
* All pitches are assigned to C right now, for QA'ing in Verovio
* Chords are taken into considerations, but not voices (assume always voice 1 for now).
* Fixes an issue with retrieving NoteRests that was present in past version.

## Version 0.02

* Keeps tracks of new key signatures and new time signatures (but assumes same key / time across all staves)

## Version 0.01

 * Generates a legal Humdrum file.
 * Retrieves Score info and correctly converts to Humdrum format
 * Dictionaries for clefs, key signatures, time signatures (including c and c| time)
 * Dictionnary for ~ half the possible instruments in Sibelius. Unmapped isntruments appear as \*I?? for the moment
 * Long and short names of instruments are recorded properly
 * Barlines with bar numbers are at correct position
 * Basic syntax to evaluate events vs null token is in place (at the moment, events are all marked as X)

ToDo
- [ ] Verify instrument changes througout the Score (currenrtly only initial _ is recorded)
- [ ] Make sure grace notes are taken into consideration
- [ ] What about multiple voices within a bar?
- [ ] Reverse staff order
- [ ] Tuplets
- [ ] Better way to deal with Whole-Measure Rests
- [ ] Create pitches dictionary
- [ ] Add support for multistaff instrument (e.g. piano) \*staff2	\*staff1 

