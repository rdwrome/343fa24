## homework?

##

## effected

- x fade

`xfade (s("bd*2"), "<0 .25 .5 .75 1>", s("hh*8"))`

- low pass filter

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>")`

- crush

`s("<bd sd>,hh*3").fast(2).crush("<16 8 7 6 5 4 3 2>")`

- gain

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").gain(1.2)

- vowel

`note ("c <c d e> e").sound("sawtooth").lpf("<400 500>").vowel("<a e i o u>")`

- room

`s("bd sd [~ bd] sd").room("<0 .2 .4 .6 .8 1>")`

- begin

`samples({ rave: 'rave/AREUREADY.wav' }, 'github:tidalcycles/dirt-samples')
s("rave").begin("<0 .25 .5 .75>").fast(2)`

## [strudel + hydra](https://strudel.cc/learn/hydra/)