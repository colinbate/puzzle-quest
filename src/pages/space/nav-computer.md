<script>
import { url } from '@sveltech/routify'
import CluelessCrossword from '~/CluelessCrossword.svelte';
import Sudoku from '~/Sudoku.svelte';
import KeywordTranslator from '~/KeywordTranslator.svelte';

const ccgrid = [
  [6, 3, 22, 21, 4, 12, 8, null, null, null, null, 20, null, null],
  [23, null, 1, null, null, 22, null, 19, 21, 9, 15, 21, 14, 8],
  [5, 11, 8, 4, 15, 8, null, null, null, 8, null, 3, null, 18],
  [8, null, 12, null, null, 9, null, 6, null, 21, null, 21, null, 6],
  [15, null, 9, null, 23, 7, 17, 24, 5, 3, null, 14, null, 24],
  [21, 19, 8, 4, null, null, null, 12, null, null, null, 21, null, 13],
  [24, null, 4, null, null, null, null, 22, null, null, null, null, null, 8],
  [null, null, 15, 6, 4, 19, 8, 24, 20, null, 16, 12, 2, 12],
  [null, 2, null, null, null, null, null, 6, null, null, null, null, null, 2],
  [13, 21, 22, 3, 10, 8, 4, 8, null, null, null, 3, null, 8],
  [null, 24, null, null, null, null, 8, null, null, 2, 8, 17, 8, 4],
  [null, 15, 2, 12, 13, 21, 5, 22, 12, null, null, 8, null, null],
  [null, 8, null, null, null, null, 24, null, null, null, null, 12, null, null],
  [12, 4, 15, 12, 8, null, 5, 20, 24, 8, 12, 4, 6, null]
];

const sgrid = [
  [{type: 'b'}, {type: 'b'}, {type: 'b'}, {type: 'b'}, {type: 'y'}, null,        {type: 'b'}, {type: 'b'}, null],
  [null,        null,        null,        null,        {type: 'b'}, null,        {type: 'b'}, {type: 'b'}, null],
  [{type: 'b'}, null,        {type: 'b'}, {type: 'x'}, {type: 'b'}, {num: 4},    null,        {type: 'y'}, null],
  [{type: 'b'}, {type: 'b'}, null,        null,        null,        {type: 'b'}, {num: 6},    null,        null],
  [null,        null,        null,        {type: 'b'}, {type: 'b'}, {type: 'y'}, null,        {num: 8},    null],
  [{type: 'b'}, null,        {type: 'b'}, null,        {type: 'b'}, {type: 'b'}, null,        null,        {type: 'y'}],
  [{type: 'y'}, null,        {type: 'b'}, {type: 'b'}, null,        null,        {num: 9},    {type: 'y'}, null],
  [null,        null,        null,        null,        null,        {type: 'b'}, {type: 'x'}, {type: 'b'}, null],
  [{type: 'x'}, null,        {type: 'y'}, {type: 'b'}, null,        {type: 'b'}, null,        {type: 'b'}, {type: 'x'}]
];
</script>

Hello again, Rhyd here!

Thank you so much for finding the keyword for my navigation computer. If you haven't found it yet, I suggest taking a look at my [original plea for help][p1].

Unfortunately, as you are probably realizing, things are never simple when it comes to me. My navigation computer is no exception. In order for it to use the keyword you found, you need to find the key. Unfortunately this isn't the type of key which might be found between the cushions of my chair, rather it is an encoding/decoding key.

All that the computer is showing me is this grid of numbers.

<CluelessCrossword data={ccgrid} />

And under that it is flashing `A-8 Earth Navigation`.

I guess once you determine the key you need to encode the keyword you found before. You can see for yourself, as the computer is also showing this:

<KeywordTranslator />

Once you figure it out, try entering it and see what happens. I believe it should give you a navigation target in the form of a country. I believe that is how you divide up your Earthen land masses.

Skimming through the manual it looks like the computer then needs to triangulate using the three most populous cities from the country. Yes, it seems that information will need to encoded and entered into this grid. It doesn't say how the grid works, hopefully you will recognize it.

<Sudoku data={sgrid} />

Once you solve that grid, it says that another city should be revealed. And that city will be where I am to meet my Earth contact. Whew, I warned you that using the computer wouldn't be very simple. I appreciate you trying to help. Let me know once you have figured out which city I am headed for.

Truly,  
Rhyd

[p1]: {$url('.')}
