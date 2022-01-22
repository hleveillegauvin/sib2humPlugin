# sib2humPlugin
A Sibelius plugin to convert Sibelius scores to Humdrum

Work in progress

## Version 0.01

 * Generates a legal Humdrum file.
 * Retrieves Score info and correctly converts to Humdrum format
 * Dictionaries for clefs, key signatures, time signatures (including c and c| time)
 * Dictionnary for ~ half the possible instruments in Sibelius. Unmapped isntruments appear as \*I?? for the moment
 * Long and short names of instruments are recorded properly
 * Barlines with bar numbers are at correct position
 * Basic syntax to evaluate events vs null token is in place (at the moment, events are all marked as X)

ToDo
- [ ] Write dictionary to convert NoteRest to Humdrum kern
- [ ] Verify key + time signature + instrument chanegs througout the Score (currenrtly only initial _ is recorded)
- [ ] Take into consideration other BarObjects
- [ ] Make sure grace notes are taken into consideration
- [ ] What about chords?
- [ ] What about multiple voices within a bar?

