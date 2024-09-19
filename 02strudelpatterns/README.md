# patterns

### samples vs synths

### n vs note
- [`n` is sometimes short for note, sometimes short for 'iNdex', so beware](https://github.com/tidalcycles/strudel/discussions/395)
  - [see also](https://tidalcycles.org/docs/patternlib/tutorials/workshop#difference-between-functions-n-and-note)

## noted

- define by midi note

`note ("48").sound("sawtooth")`

- or pitch name

`note ("c3").sound("sawtooth")`

- sequence away

`note ("c2 d3 e2").sound("sawtooth")`

- sequence over multiple cycles

`note ("[c d e]/4").sound("sawtooth")`

- play one per cycle

`note ("c <c d e> e").sound("sawtooth")`

- scale

`n("0 2 4 6 4 2").scale("C:major").sound("sawtooth")`

**everybody now!**

## share a midi sequence

## [sometimes and its cousins](https://tidalcycles.org/docs/reference/randomness/#the-sometimes-family)

## transformations

- loop at

`samples({ rhodes: 'https://cdn.freesound.org/previews/132/132051_316502-lq.mp3' })
s("rhodes").loopAt(2)`

- degradeBy

`s("hh*8").degradeBy(0.2)`

- struct

`note("c,eb,g")
  .struct("x ~ x ~ ~ x ~ x ~ ~ ~ x ~ x ~ ~")
  .slow(2)`

- mask

`note("c [eb,g] d [eb,g]").mask("<1 [0 1]>")`

- palindrome

`note("c d e g").palindrome()`

## sophisticated rhythms

- linger

`s("lt ht mt cp, [hh oh]*2").linger("<1 .5 .25 .125>")`

- euclid

`note("c3").euclid(3,8)`

## effected

- x fade

`xfade (s("bd*2"), "<0 .25 .5 .75 1>", s("hh*8"))`

- low pass filter

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>")`

- 'gain'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").gain(1.2).vowel("<a e i o u>")`

- 'vowel'

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").vowel("<a e i o u>")`
