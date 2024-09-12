## pattern transformations

- echo

`s("bd sd").echo(3, 1/6, .8)`

- degradeBy

`s("hh*8").degradeBy(0.2)`

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

## share a midi sequence

## effected

- low pass filter

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>")`

- 'gain'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").gain(1.2).vowel("<a e i o u>")`

- 'vowel'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").vowel("<a e i o u>")`
