## Strudel is based on [TidalCycles](https://tidalcycles.org/)
- [Everything is pattern-based](https://tidalcycles.org/docs/reference/cycles)
- Uses JavaScript in the browser (so you don't have to download anything!)
- Not quite as powerful as TidalCycles...


## starter pattern commands and syntax
`s` = sound

`" "` = what to fit inside one cycle

`~` = silence

`!` = repeat

**starter examples**

`s ("bd")`

`s ("bd hh")`

`s ("bd ~ hh")`

`s ("bd ~ hh!2")`

**everybody now!**

## more advanced commands and syntax

`[]` = nest these within one pulse of the cycle

`,` = layer these atop one another within one cycle

`[ | ]` = randomly choose sample from this list per cycle

`?` = randomly silence

`( , )` = spread this many pulses over this many pulses per cycle

**more examples**

`s "(bd ~ [hh!2]")`

`s ("bd, ~ hh")`

`s ("[bd | hh | sd]!4")`

`s ("hh!16?")`

`s ("bd(7,12)")`

**everybody now!**

## stack

`stack (s (" "),
s (" "))`

**stack of example**

`stack (
s ("bd(7,12)"),
s ("hh!16?")
)`

**everybody now!**

## noted

- define by midi note

`note ("48").sound("sawtooth")`

- or note name

`note ("c").sound("sawtooth")`

- sequence away

`note ("c d e").sound("sawtooth")`

- sequence over multiple cycles

`note ("[c d e]/4").sound("sawtooth")`

- play one per cycle

`note ("c <c d e> e").sound("sawtooth")`

**everybody now!**

## effected

- low pass filter

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>")`

- 'gain'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").gain(1.2).vowel("<a e i o u>")`

- 'vowel'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").vowel("<a e i o u>")`