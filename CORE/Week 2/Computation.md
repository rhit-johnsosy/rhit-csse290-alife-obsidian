URL: https://samwho.dev/turing-machines/

Turing machine consists of 4 parts and 5 instructions:

Parts
1. a tape
2. a head
3. a program
4. a state

Instructions
1. P - prints a given symbol to the tape
2. R - moves the tape head right
3. -> - jumps to a given state
4. L - moves the tape head left
5. R - halts the machine

"Everything you have ever seen a computer do can be done with a Turing machine."


What does it mean to compute?
* Something is said to be "computable" if there exists an algorithm that can get from the given input to the expected output.

"Components that switch between 2 states are cheaper, smaller, and more reliable than components that switch between 10. It was more practical to build computers that worked in binary than ones that work in decimal, though attempts to build decimal computers [were made](https://en.wikipedia.org/wiki/Decimal_computer)"


What can't be computed?
* The "Halting problem"
	* "Given a program and some input, is it possible to write a second program that will tell you with certainty whether the first program will halt or run forever?"
		* Answer is no.

What does it mean to be Turing complete?
* "A system is Turing complete if it can be used to simulate a Turing machine."

"When someone says something is Turing complete, what they mean is it _would_ be Turing complete if it had an infinite amount of memory. The infinite tape limitation means no Turing machine could ever exist in our physical reality, so that requirement tends to get waived."

"If you watch the program run to completion, something that might strike you is just how much work is required to do something as simple as adding 2 numbers. Turing machines were not designed to be practical, Turing never intended anyone to go out and build one of these machines in the hope it will be useful.

Modern machines have circuits within them that can add 2 numbers together by passing 2 electrical signals in and getting the sum as a single signal out. This happens in less than a nanosecond. Modern machines have memory where any byte can be accessed at any time, no tape manipulation required. This memory access takes a few dozen nanoseconds."


Writing and running your own programs
"I've built a web-based development environment for writing programs that will run on the Turing machine visualisations you've seen throughout the post.

You can access the editor **[here](https://samwho.dev/christopher)**."

Time: 15 minutes