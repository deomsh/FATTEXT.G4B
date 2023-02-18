FATTEXT.G4B v0.2 (20230218), by deomsh

Highlights:
- Opening of existing text-files from command-line
- Opening of text-files from menu, browser included
- History of opened files included - max 9 files
- Saving of text files to FAT devices, Save As available
- Backup of text files, different name possible, inside editor original name unchanged
- Numbered lines, goto line number available
- Write/ Add/ Insert/ Edit single lines (max 511 chars)
- Auto-split lines from 470 chars and above
- Join lines (backwards)
- Display lines up to 1554 chars
- Select/ copy/ cut/ paste line, multiple lines too
- Full grub4dos' History Buffer available
- Original line copied to History Buffer if Edit/ Copy/ Cut a single line (up to 1533 chars)
- Find string in text file, max 80 chars, number of 'finds' displayed
- Replace/ Delete found string
- Convert text file type to MS-DOS (default), Unix or (old) Mac
- Change color: 28 presets available - original color restored after closing
- Change graphicsmode (640x480 only, 25 lines used) - original color/ graphicsmode restored after closing
- Saving of configuration and file-history to FATTEXT.DAT

Function: Write and Edit text-files
          Saving on fat-devices only - Filesize max 261631 Bytes (MS-DOS type)
          Grubutil 'fat' needed
          Installed memory >= 72 MB

Use:      FATTEXT.G4B [/MDBASE:address]
          FATTEXT.G4B [/MDBASE:address] [[DEVICE/]PATH/]FILE
          FATTEXT.G4B /?

Switch:   Changes start address of memory in use, >= 0x3000 (default), 0x1000 sectors needed (2MB)

Remarks:  Without device/ path, file on/ from root - '/' not mandatory
          Names 8+3 only only, End Of Line Marker: MS-DOS, Unix or Mac Type
          Settings saved to FATTEXT.DAT, OR some variables not erased after closing
          Zero's in file refused (hex: '00'), warning if detected in file while in memory, backup file if still possible
          Backups found on (fd99), original files in root, last savings in 'LASTSAVE'
          After a crash, copy desired backups from (fd99) with Grubutil 'fat'
          Virtual floppy in use: (fd99), unmapped if exists already!
          Grubutil FAT needed in (bd), (bd)/boot/grub, (bd)/grub, (bd)/g4dll or on root
          Original status of debug, pager, graphicsmode and color restored afterwards
         
Tricks:   Use ArrowUp for editing, all single edited/copied/cut lines in History
          Underscore is placeholder for ONE starting space BEFORE ALL other chars
           spaces in between and after other chars accepted normally
          Replace is active after a Find, to insert new replace-string use Ctrl+R
          To start with color-preset use menu-item Graphics in Main Menu

History:
v0.2
First published version
