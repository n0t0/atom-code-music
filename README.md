# Atom MIDI Piano

Play music notes like a piano while typing in Atom.

`Ctrl` + `Alt` + `p` or use command `atom-midi-piano:toggle` to toggle.

Default is Music Box Mode, you can also switch to Real Piano Mode in settings.

Keymap manual is under preparing...

## About the converter.

### How to add custom music sheets.

If you can write music sheets in digit-sheets, you can use the `atom-midi-piano:convert` command to convert it into coffeescript/javascript array music sheet, which is used to record built-in music sheets.

First write correct digit-sheets with following mode:

\(low-music-key\)    middle-music-key    \[high-music-key\]    {double-higher-music-key}    \<chord-note1 chord-note2\>

**Warning:**

1. Only `<` `>` can be mix in to the other three brackets, or it will trigger an error.

2. Do not use cross-line brackets, you'd better to close and reopen a pair of brackets at line end/beginning to prevent strange error. (Here line is soft warp in Atom, not hard warp in file.)

**Usage:**

1. Open your digit-sheets, then use command `atom-midi-piano:convert`, it will open a untitled buffer and convert it into a coffeescript/javascript array music sheet.

2. Save the array sheet with `.coffee` or `.js`. Add the saved file path into `lib/sheets-list.coffee` as a member of the array. Reload Atom.

**Choose custom music sheets in settings will be added in future.**
