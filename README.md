# Simple AI Connect 4
This is a simple JavaScript implementation of a reinforcement algorithm which simply weights states 'visited' in order to win, and reduces weights visited on a loss.  Draw has no effect.

The permutations of options are in the billions for a full board, so the board can be set to smaller (4x4 is the smallest possible).

## How clever are the players after 2000 iterations?
Not very.

The permutations are still pretty large, so it hasn't seen the same conditions sufficiently to make a judgement to lower or increase weights.

This is not very fast, and doesn't have any hashing of the board to consider similar states such as a mirror image or shifted left/right.

## Bugs
There is some bug somewhere which allows a play a non-existent column on the far right (or possible a negative one on the left) which crops up, but I can't find what it is.  That's what I get for not writing any tests for this.

## Why?
Why not?

This was inspired by the Royal Institution Christmas Lectures which had a match-box powered Noughts and Crosses player which used the same algorithm (but used beads for moves, rather than columns as I have).  
