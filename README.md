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


## Problem J4: Flipper

Depending on how one approaches J4, the problem can either be surprisingly straightforward or needlessly tedious. (In this overview, I will only be going over my more efficient solution but if you simply read through the problem, you should easily find the less efficient methods as well) The problem begins with a 2x2 grid with numbers 1 through 4. This initial positioning is identical regardless of input. Then, a series of operations - inputted as characters 'H' or 'V' in a string - manipulate the ordering of these numbers by flipping the grid vertically or horizontally. We are tasked with outputting the final layout of the grid. In my solution, I realized that there only 4 states of the grid that could be outputted. Possibly even more important than that, I realized that these 4 states were no more than the result of 2 binary parameters - horizontal and vertical flip state. As the flipping operations to not actually affect horizontal layout, I simply considered each individually. Additionally, 2 flips in the same direction always cancel each other out. Now, for the solution, I simply counted the number of horizontal and vertical flips. Then, by taking the remainder of these counters when divided by two, I found the effective number. of horizontal and vertical flips (either 0 or 1 for each / flipped or not flipped). Now, I simply outputted 4 integers in a grid, but each had a unique algorithm to give the correct value based on the number of H/V flips. For example, the first position which began at 1 could be written as 1+2V+H, where V is the number of vertical flips and H is the number of horizontal flips. This is because after a vertical flip the top andbottom rows are exchanged and the numbers on the bottom are 2 greater than those above. The horizontal flip is the same but the numbers on the right are only 1 greater. Thus, with a simple counter and well-designed algorithm, J4 can feel like the easiest problem on the contest.

Difficulty - 2/10

## Problem J5: Rule of Three

J5 is significantly harder than any other question on this contest, or most other hgih school coding contests in general. I believe there are multiple ways to approach it, especially depending on the language in use, but within the constraints of Java, I immediately turned to a recursive solution.
