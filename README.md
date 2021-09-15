# CCC2019

Arun Atchuthananthan
CCC Junior 2019 Thoughts
Score - 75/75

## Problem J1: Winning Score

J1 was very straightforward. The input was 6 positive integers with values under 100. The 6 inputs were divided into 2 3-integer halves - eahc of which corresponded to the number of 3, 2, and 1 pointers team Apple and Banana scored, respectively. We were tasked to identify which team won, which I did by multiplying the inputted integers by the point-value fo the basket they represented (3,2,1) and then summing the 3 products for each team. The team with the greater result won.


## Problem J2: Time to Decompress

I solved question J2 with a simple implementation of loops. Essentially, we received a number of lines of input (or as it pertained to my code, the number of iterations of my input and later solution loops). Consequently, that many lines would be inputted, each with a symbol and number. My solution created a 2 arrays, whose sizes corresponded to the initial number input, and stored each symbol/number in corresponding positions within the two arrays. I then looped through the arrays and at each index I printed the symbol repeatedly according to the number inputted alongside it. As long as one ensured that left a line break at the end of each symbol-printing loop, J2 should have presented no issues.
