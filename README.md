# Simple AI Connect 4
This is a simple JavaScript implementation of a reinforcement algorithm which simply weights states 'visited' in order to win, and reduces weights visited on a loss.  Draw has no effect.

The permutations of options are in the billions for a full board, so the board can be set to smaller (4x4 is the smallest possible).

## How clever are the players after 2000 iterations?
Not very.

The permutations are still pretty large, so it hasn't seen the same conditions sufficiently to make a judgement to lower or increase weights.

This is not very fast, and doesn't have any hashing of the board to consider similar states such as a mirror image or shifted left/right.

## How can I see it in action?
You can view this in this repository [GitHub Pages](https://loz.github.io/ai_connect4/).

The JS will run 2000 itterations and then show the moves the players are making for each run from there.

## Bugs
There is some bug somewhere which allows a play a non-existent column on the far right (or possible a negative one on the left) which crops up, but I can't find what it is.  That's what I get for not writing any tests for this.

## Why?
Why not?

This was inspired by the [2019 Royal Institution Christmas Lectures](https://www.rigb.org/christmas-lectures/2019-secrets-and-lies)
which had a match-box powered Noughts and Crosses player which used the same algorithm
(but used colured beads for moves, rather than an array of columns as I have).  
