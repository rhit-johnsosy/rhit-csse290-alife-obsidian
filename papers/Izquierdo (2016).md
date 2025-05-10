
URL: https://www.sciencedirect.com/science/article/abs/pii/S0959438816300691


* Behavior arises from the interaction between neural activity, body and environment.
- _C. elegans_ is an ideal organism for whole-animal modeling.
- "successful whole-animal modeling requires an animal for which detailed behavioral, biomechanical and neural information is available and a modeling methodology which can gracefully cope with the constantly changing balance of known and unknown biological constraints"
- full name: _Caenorhabditis elegans_

* Nervous system? (lots of questions around nervous system were brought up)
	* What it is for 
		* coordinate the behavior of a multicellular animal (furthers the reproductive success of the species)
* central challenge of 21st century systems neuroscience: move beyond individual neurons and small circuits and regions 
* "_C. elegans_ is perhaps the best characterized animal in the world."
	* first animal to have its genome fully sequenced
	* **only** animal to have its complete developmental cell lineage and neural connectome mapped
	* extensive graph theoretic analysis of the structure of C. elegans connectome has been performed

### The Electrophysioslogical Challenge
* "Of course, connectivity alone is insufficient for understanding neural activity and its role in behavior [11]; electrophysiological and neuromodulatory information is also required and the data here are much less complete."
* considerable progress in whole-cell patch clamping techniques over the last decade
* functional properties can sometimes be inferred from
	* gene expression mapping
	* behavioral genetics
	* laser ablation
* "Perhaps the most exciting recent development in C. elegans electrophysiology is the increasingly sophisticated ability to optically image and manipulate large-scale neural activity at the cellular level in the intact worm."
* " Kato et al. [18**] have recently identified a low-dimensional intrinsic neuronal oscillation whose segments may encode distinct action sequences and their parameter"

### Models of Locomotion
First paragraph of the section titled Models of Locomotion is a great defense for having models throughout any research. As such, here is the whole paragraph:
* "Modeling plays an essential part in any nontrivial integrative endeavor. All too often, however, modeling is seen merely as a capstone of an experimental program, a final confirmatory step that all the essential pieces have been identified. But models embody theories and, as such, they should be an equal partner with experiment from the very beginning of a research program. The very act of formulating a model helps to identify gaps in the experimental knowledge that need to be filled."
* "**A model is a failure only if it teaches us nothing new."**
* C. elegans moves by "propagating dorso-ventral bends along its body with a wavelength that depends on the properties of the medium through which it moves."
* Models of locomotion divided into those that
	* include a neuronal central pattern generator in the head
	* those that rely on sensory feedback mechanisms to generate the rhythmic pattern
* Niebur and Erdos the first to create an integrated neuromechanical model of forward locomotion
* To read about a model:
	* " Most recently, Boyle, Berri and Cohen [42] developed a neuromechanical model of locomotion using realistic environmental forces (Figure 2A, B). The model was designed to produce and propagate the waves using proprioceptive feedback. The results of the model lead to experiments that have strengthened the evidence for the role of proprioception in the control of undulations [43]. The model reproduced the transition from swimming to crawling using a single gait, **providing testable predictions** about the modulation of neuromuscular control as a function of the resistivity of the environment, some of which have been verified [24].  "

### Models of Spatial Orientation
* "Spatial orientation behaviors are fundamental for any animal."
* "Within the context of odorants, tastants, and temperatures, two main strategies have been studied: klinokinesis and klinotaxis"
* "Klinokinesis involves a biased random walk. On agar, a forward crawl is interrupted by sharp turning events called “pirouettes.”"
* Successful example:
	* "Most recently, Roberts et al., [57**] developed a stochastic model involving two highly idealized populations of the forward and command motor neurons that reproduces the kinematics of the biased random walk using a point model of the worm’s body. After adjusting the model to reproduce behavior, the model predicted key aspects of the functional connectivity between the neurons involved. These predictions were then confirmed using photoactivation and electrical recordings from the key motorneurons."
* "Klinotaxis involves gradual turns toward the line of steepest ascent up a gradient by modulating rhythmic head oscillations as a result of changes in stimuli that must be detected by sensory neurons within the timescale of a head sweep"
	* First model of sensorimotor basis of klinotaxis
		* utilized a highly idealized biomechanics and neural circuitry
			* " focusing on demonstrating a minimal circuit capable of modulating the dorsoventral oscillatory pattern required for steering during locomotion"

### Conclusion
" Once again, C. elegans can lead the way on a fundamental biological problem, this time to the development of a systems neuroscience that does full justice to the brain-body-environment interactions that underlie the operation of animals as integrated wholes. "



Yoder's example of proprioceptive feedback:
* Fall and break your ankle
	* Why is your chance of breaking it higher?
		* It is **NOT** because you broke it but because your inner perception, your balance, has changed
* Proprioceptive feedback refers to the feedback related to your own inner perception of self


**New developments question:**
Weights between neural networks not known yet and thresholds.

EEs have to poke neurons w/ electrodes to map the profile of the neuron. Has been done to 5 neurons out of 302. They are pressurized and tend to pop and burst. 

It's the best one. 

None of the worm people think that a full mapping of electrophysiology can be done.

Certain proteins that fluoresce can be injected into the worm, go into different neurons, creating a rainbow of colors in the neurons, you know by the color -- RGB -- which neuron it is. You can put it under the microscope and see it happen in real time. You can also do this using lasers. An approximation of how neurons affect each other neuron through this, optogenetics. Will be hard, but is possible. There are people who don't believe in this, big data isn't enough to understand the innerworkings. Poking is the plan for the next 10 years.



**LLMs effect question:**

Good thing:
* More people interested in research.

Bad thing:
* Poking came from this type of big data LLM-type people. Good in a way, but pushes it in a way that may push us forward but may not fully grasp things in an understandable way. 
	* Nobel prize for replicating it but not extendable to other parts of science.

Lots of people focusing on the worm, but still mostly alone on his focused path.

No downside to more people taking a look at a problem. **Take all the approaches.**


**Notes from Alex question:**
* Hope of understanding the worm is that it reveals underlying properties of all organisms
	* Only have to fully dissect one organism to greatly reveal the properties of others
* Step forward
	* There is an immense amount of variability in biology. 
	* Biology is messy.
	* CS is cleaner.
	* Evolution is degenerate
		* Taking a leg off a salamander is able to operate
	* Biologists don't want to think of variability - "one model for this thing"
	* "Worms are pretty amazing, better than phones, and definitely better than ChatGPT."
	* **Understand variability**
	* **Better technology**
		* Much better than our laptops (bio-inspired)

**Notes from Dominic questions:**
* Gradient descent algorithm
	* From someone's brain in the 1950s
	* Used in ChatGPT
	* Not happening in living organisms
	* Not in C. elegens
	* That feedback isn't there
* How are the worms modelled in 3D?
	* Simulations tend to be 2D as the data is limited to the data taken from the C. elegens in an agar plate
	* Has been an attempt at putting a worm in a cube
	* 3D modelling has been happening in the last 3 years
		* Moves in a coil
	* Eduardo is choosing to ignore the 3D as life is too short (life, tennis, cake)
* Eduardo's overall approach is understanding the intricacies of each step before adding dimensions or additional complexity.