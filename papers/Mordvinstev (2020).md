https://www.youtube.com/watch?v=kA7_LGjen7o&ab_channel=ODSAIGlobal
follow-along didn't get very far

"Generally speaking, differentiable self-organizing systems consist of a neural controller that is shared by a population of agents interacting on a simulated environment. During a limited time span the whole system is evaluated against an objective function that measures the proximity of the current behavior to the desired."![[{1613E2BB-52A2-4C24-B73A-1A8A38BAB633}.png]]
 "End-to-end differentiability allows propagation of the objective gradient to the controller steering the system behavior towards the target specification."![[{422EC8C0-D629-4605-8AD7-E246FD4E897F}.png]]
	"Neural CA operates on a uniform grid the state of each cell is represented by a number of real values, three of which are visible as RGB color channels. Cells iteratively update their state using the information collected from their three by three neighborhood."![[{EC9E7882-EDA4-4E78-A59C-9ED66EF199B6}.png]]
- Grow a pre-defined pattern starting from a single seed cell



https://distill.pub/2020/growing-ca/
* Morphogenesis
	* process of an organism's shape development
	* striking example of self-organisation
	* same aspect was emulated in the Minecraft example I brought up last week [[Week 5.pdf]]
	* surprisingly adaptive 
		* ex: some organisms when cut in two end up becoming two independent organisms
* CAs typically consist of a grid being iteratively updated
	* despite their simplicity, usually result in rich, interesting behaviors
* ![[{C07EB3B2-F647-4956-A052-804FCF705F8C}.png]]
* each cell state represented as a vector of 16 real values
	* first three represent colors visible to us
	* target pattern has color channel values in range 0.0-1.0
	* alpha symbol equal to 1.0 for foreground pixels and 0.0 for background
		* cells having an alpha of > 0.1 are considered living and so are their neighbors
		* others are dead and have their state vector set to 0
		* therefore, 0.1 is the living threshold
	* hidden channels don't have a predefined meaning

* CA rule
	* Perception
		* defines what each cell perceives of the environment around it
		* implemented with a 3x3 convolution with a fixed kernel
	* Update rule
		* every cell runs the same update rule
		* outputs an incremental update to the cell's state
	* Stochastic cell update
		* random per-cell mask to update vectors
		* used to mimic the randomness of real life
	* Living cell masking
		* explicitly setting all channels of empty cells to zero to avoid any hidden states

### Experiment 1: Learning to Grow

![[{304831C8-CF81-4653-9DB3-F53875F3F683}.png]]

* illuminates different challenges by presenting the model without any fixes yet
* approach: optimize the update rule using backpropagation-through-time, select best model of each, run for steps beyond what was trained on and see what happens
	* results vary by model (inconsistency between models)

### Experiment 2: What persists, exists

* one strategy to fix the instability is to train for more steps
	* not optimal due to longer training time and memory requirements
* "sample pool" based strategy 
	* define a pool of seed states to start the iterations from, initially filled with the single black pixel seed state
	* then sample a batch from this pool which we use in our training step
		* to prevent the equivalent of "catastrophic forgetting" we replace one sample in this batch with the original, single-pixel seed state
	* after concluding the training step, replace samples in the pool that were sampled for the batch with the output states from the training steps over this batch
	* random dynamics in the system allow the model to end up in strange states near the start of the training process
	* over further samples, refine the dynamics to recover from those states
	* as the model becomes more robust at going from a seed state to the target state, samples in the pool reflect this and are more likely to be very close to the the target, allowing further refinement from the training
	* In other words, we use the previous final states as new starting points to force our CA to learn how to persist or even improve an already formed pattern

![[{CD15B7AD-0601-4D36-9531-D46697DF7C5F}.png]]

### Experiment 3: Learning to regenerate 

* After experiment 2 can properly grow but not regenerate

![[{9856477D-AAAE-4445-9277-E5A4E42B2240}.png]]

* "We let each of the models develop a pattern over 100 steps, then damage the final state in five different ways: by removing different halves of the formed pattern, and by cutting out a square from the center."
* lizard develops strong regenerative capabilities w/o being explicitly trained for it
* The systems were trained to grow, stabilize, and never entirely self-destruct but were then open for a variety of possibilities: regeneration, explosive mitosis (uncontrolled growth), unresponsiveness to damage (overstabilization), or even self destruction
* Solution: increase the basin of attraction for our target pattern - increase the space of cell configurations that naturally gravitate towards our target shape
	* accomplished by damaging a few pool-sampled states before each training step
	* sample 8 states from the pool
		* replace highest-loss sample with the seed state
		* damage the lowest-loss states by setting a random circular region within the pattern to zeros

### Experiment 4: Rotating the perceptive field
* "As previously described, we model the cell’s perception of its neighbouring cells by estimating the gradients of state channels in x⃗ and y⃗ using Sobel filters. A convenient analogy is that each agent has two sensors (chemosensory receptors, for instance) pointing in orthogonal directions that can sense the gradients in the concentration of certain chemicals along the axis of the sensor. What happens if we rotate those sensors? We can do this by rotating the Sobel kernels." -- quoted because this is my first time coming across Sobel kernels
* Rotating pixel based graphics involves computing a mapping that's not necessarily bijective and classically involves interpolating between pixels to achieve the desired result.
	* This is because a pixel, when rotated, will now likely overlap several pixels.
	* Successful growth in some rotations suggest a certain robustness to the underlying conditions outside of those experienced during training