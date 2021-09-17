# CCC2019

Arun Atchuthananthan

CCC Junior 2019 Thoughts & Review

Score - 75/75

Note: My solutions to this contest were written in Java, as it was a language I was practicing at the time and seemed capable of handling the given questions. There are likely several other solution methods which I have not outlined below. If you have any comments on my solutions or even further suggestions in other languages, I would love for you to reach out.

## Problem J1: Winning Score

J1 was very straightforward. The input was 6 positive integers with values under 100. The 6 inputs were divided into 2 3-integer halves - eahc of which corresponded to the number of 3, 2, and 1 pointers team Apple and Banana scored, respectively. We were tasked to identify which team won, which I did by multiplying the inputted integers by the point-value fo the basket they represented (3,2,1) and then summing the 3 products for each team. The team with the greater result won.

Difficulty - 1/10


## Problem J2: Time to Decompress

I solved question J2 with a simple implementation of loops. Essentially, we received a number of lines of input (or as it pertained to my code, the number of iterations of my input and later solution loops). Consequently, that many lines would be inputted, each with a symbol and number. My solution created a 2 arrays, whose sizes corresponded to the initial number input, and stored each symbol/number in corresponding positions within the two arrays. I then looped through the arrays and at each index I printed the symbol repeatedly according to the number inputted alongside it. As long as one ensured that left a line break at the end of each symbol-printing loop, J2 should have presented no issues.

Difficulty - 2/10

## Problem J3: Cold Compress

J3 is slightly more complicated than the first two problems, as one might consider how to solve the problem efficiently. Unlike the previous two, the looping solution in J3 is meant to identify characters sequences of unspecified within an input string. Thus, I approached the problem from the perspective of using a while loop, as such a loop could loop until a condition is satisfied rather than a specified amount of times. This is useful in this case as I used the exit condition for the while loop to be that the character in the current position (as I am looping through each input string character by character) does not equal the next character. In this case, I store the repeated character in an array with the integer consecutive character counter (that was increasing by 1 for each successful loop) in the correlating position of another array. At the final position of the string, I store the data for the final character sequence and then loop through the two arrays, outputting the stored characters and counters with relevant styling. As long as one avoids edge case errors (such as overlooking single character sequences or miscounting characters at the end of each string), the use of a while loop and counter should lead contestrants to a fairly simple solution. I also later optimized this program in Java by using String lang libraries and preexisting character locating fucntions. Though, in using these one must not become oblivious to their limitations (example error could involve combining two separate sequences of the same character).

Difficulty - 3/10
