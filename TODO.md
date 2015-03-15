# TODO #

At the moment, ndstrim is a second generation trimmer. That means it intelligently looks in the header of the rom file and finds out how big the rom data is, excluding the unnecessary space at the end of the rom.

These are the things we want to do:
  * Some reports indicate some roms don't have the romsize data in the rom header, ndstrim should check for this. _High priority_ **Implemented in CLI but not Ruby CLI/GUI**
  * Make ndstrim look up the internal rom name, can be useful for end user to see. _High priority_
  * Implement better command line syntax. Both single operation and multiple file operation should be possible, with ability to specify output directory and/or add prefix/suffix to output filename. _High priority_
  * Look into other trimmers and see what techniques are used. _High priority_
  * Add a progress bar to the GUI. _Medium priority_
  * Implement first-gen trimmer which is used if the romsize data couldn't be acquired. _Medium priority_
  * Do better reliability checking. E.g. checking if there are anything other than 0x00 or 0xFF after the determined romsize. _Medium priority_
  * Support stdin and stdout. _Medium priority_
  * Manually supply correct romsize values for troublesome roms. To be determined if this is a good solution. _Low priority_
  * Make the code [endianness](http://en.wikipedia.org/wiki/Endianness) independent. Currently it will probably only work on little-endian machines. _Low priority_
  * Make the GUI display the internal rom icon ([technical info](http://nocash.emubase.de/gbatek.htm#dscartridgeicontitle)). _Low priority_