
URL: https://ar5iv.labs.arxiv.org/html/1810.01870

"Sensorimotor contingency theory offers a promising account of the nature of perception, a topic rarely addressed in the robotics community." 
* Why is it rarely addressed?

Three preliminary applications presented to illustrate the approach to the acquisition of perceptive abilities: 
* discovering the environment
* discovering objects
* discovering a visual field


### Introduction

Perception in robots is usually handled through the hand design of feature extraction and classification algorithms. Allows for a range of complex tasks like
* object recognition
* grasping and manipulation
Limitation: Vast majority are developed to solve specialized tasks, turn out to be inefficient or completely useless when faced with unexpected situations. 
* "fundamental problem: perceptual concepts that are defined by designers, instead of being constructed by robots and grounded in their experience, are inflexible, and thus cannot engender autonomy"

Authors believe this shortcoming is due to the overfocus on **how to perceive** rather than **what is perception.** 
* what is perception, seen as a preliminary step to overcome current limitations and endow artificial systems with genuine perception
* requires middle ground between traditional hand-coded approach and behaviorist approaches

"Coming from outside the realm of robotics, the seminal paper [[6](https://ar5iv.labs.arxiv.org/html/1810.01870#bib.bib6)] introduced sensorimotor contingencies theory (SMCT) as a groundbreaking account for the nature of perception"
* refers to Kevin O'Regan's paper
* slow spread due to two reasons:
	* requires a paradigm shift from traditional approaches
	* the theory still lacks clear formalization, leaving its implementation on robots an unsolved problem

Studies on animals and humans suggest that perception is gained on an epigenetic timescale.
* With this info, traditional robotics -> developmental robotics framework where the robot, as an embodied agent, should explore the world and incrementally build its own way to perceive and interact with it. Requires a minimal set of mechanisms and constraints that are generic enough to fit various scenarios.

Propose predictive modeling as a computational model to learn sensorimotor contingencies and acquire perceptive skills.
* allows for incremental acquisition while still being computational

### Developmental Framework for SMCT

1. SMC defines a perceptive ontology
2. Predictive modeling as computational implementation of contingencies
3. An approach to allow a naive agent to build its own predictive models, and interpret the world with which it interacts

"We define perception as the ability to categorize sensory inputs based on the way they can be actively transformed by the agent."

"In order to adapt its actions, the agent must instead learn how sensory inputs can be actively transformed by its motor commands. Then the agent can process any sensory input, by predicting these transformations, and potentially selecting the best action to reach a goal state (i.e. a different, target sensory input). Thus, for the agent, **a sensory input is not relevant by itself, but only through the potentiality of transformations it allows in the sensorimotor space**."

Key part of this approach:
* "sensory inputs can be transformed in specific ways depending on the actual property of the environment they encode" - contingencies

"For the agent, mastering a contingency means knowing the corresponding sensorimotor transformation."

Key definition:
* In robotics and neuroscience literature, the encoding of knowledge relating sensory to motor information in a system (artificial or biological brain) is referred to as _internal modeling_ [[16](https://ar5iv.labs.arxiv.org/html/1810.01870#bib.bib16)].

It's often assumed that robots know everything going on in the internal model, however, there are likely some hidden factors at play.

![[{39EF66B0-FA81-42AB-A197-E57E551FF3F8}.png]]


![[{9811D13C-737F-406A-A352-5E4F864D0CA7}.png]]

A naive agent faces a couple problems when learning sensorimotor contingencies:
* needs a compact, efficient encoding of knowledge about the contingent transformation of sensorimotor states
* has to discover by itself _what_ is predictable, and _when_ this is the case

"In order to learn a contingency, the agent therefore has to build a predictive model that captures the highly probable set of sensorimotor states and transitions that define the corresponding subgraph. It can use this model to identify the contingency the next time it is encountered, and statistically predict what would be the sensorimotor outcome of its actions as a walk into this subgraph."
* this allows for related graphs or new spaces to be built on top off one another, allowing for a hierarchy and the ability to capture higher-level contingencies

![[{9D5BD9C3-BED0-4D81-B302-09BEF9AFD958}.png]]

![[{E52013B0-1AE2-4E74-AFCB-E52A6F585478}.png]]




### Preliminary Applications

Three of them, all address a different perceptive capacity:
* perception of the environment
* perception of objects
* acquisition of a visual field


#### Discovering the environment

* To begin doing this, they use the system in Fig. 2
	* simple agent-environment system
	* one motor that controls the position of one sensor, sensible to the distance to a wall that constitutes the environment.
	* From an internal point of view, the agent’s experience reduces to a manifold in its sensorimotor space, representing the sensorimotor print of the environment (see Fig. [2](https://ar5iv.labs.arxiv.org/html/1810.01870#S2.F2 "Figure 2 ‣ II-C Learning predictive models for SMC ‣ II A developmental framework for SMCT ‣ Grounding Perception: A Developmental Approach to Sensorimotor Contingencies")).

![[{E33453D2-80CA-45FA-8149-E271D503A41F}.png]]

Whole block of text that explains spectral clustering (pasted here as I need to reread it as I don't fully grasp what it means):
* "Spectral clustering finds a partitioning of the rows in T, corresponding to densely connected sub-graphs in the corresponding graph. This partitioning corresponds to candidate hypotheses of sensorimotor contingencies. The outcome of the algorithm is a classification of sensorimotor states (Si,Mk): each (Si,Mk) belongs to a cluster Xp which itself belongs to a subgraph Ya. A visualization of the final clustering for a set of 15 different environmental states is presented in Fig. [2](https://ar5iv.labs.arxiv.org/html/1810.01870#S2.F2 "Figure 2 ‣ II-C Learning predictive models for SMC ‣ II A developmental framework for SMCT ‣ Grounding Perception: A Developmental Approach to Sensorimotor Contingencies"). Note how the different subgraphs Ya internally correspond to the different environmental states that can be observed from an external point of view. As a result, each sensorimotor state is correctly associated with the corresponding environmental state that generated it (internally represented by Ya)."

The final clustering into subgraphs is only successful if the "probability of experiencing a environmental change is lower than the probability of active motor changes during the exploration phase."

"Given the current algorithm, the agent statistically clusters each point in a single meta-state. Some extensions of the algorithm are under development to determine that sensorimotor states can belong to multiple meta-states."


#### Discovering objects

![[{1EEFC539-25D4-4F89-ACC2-021E7F2F5506}.png]]

* Addresses the question of *how a naive agent can discover the concept of objects*
* Description of object: "a part of the environment that can be moved, or even be encountered in different environments"
* Translated into sensorimotor definition: "an object is a consistent subgraph defined with differential sensorimotor transitions (Si,Δ​Mq→Sj). This way, the object can be experienced from different starting motor states."


* Objective: get a naive agent to build internal representations of objects as subgraphs
	* agent lives in a 2D world
	* environment made of square elements w/ random properties represented by a single value
	* environment can randomly change
	* agent equipped w/ a sensor that captures the values of 3x3 neighbors elements to generate a 9D sensory input
	* two motors that translate the motor horizontally and vertically

![[{6F3901A6-AF02-434B-9EA0-D9DF1FE5C7B2}.png]]

* To reduce computational cost, only "salient" sensory states S_i are actually stored during the initial exploration (step 1)

* Algorithm's outcome is a classification of S_i into subgraphs
	* results presented in Fig. 3
	* "When recognizing a sensory inputs as part of an object, the agent can predict which sensory input it would receive by navigating into the corresponding subgraph"

#### Discovering the visual field

![[{0ACDC442-DAD3-4123-9BE2-8ABB2D408A3B}.png]]

* sensorimotor contingencies approach covers more than just environment recognition, as was presented in the previous two examples.
	* "also **proposes to ground the perception of the agent's own body and ability to interact with the world**"
* address the problem of perceiving (in the sense of mastering) the visual field associated w/ a visual sensor

* simulation inspired by human visual apparatus in which the retina is covered by multiple receptive fields

* agent equipped w/ a camera and two motors
* camera spans only a narrow part of the environment

![[{7C72E069-FB52-418D-B404-069865668319}.png]]

"The simulation results are presented in Fig. [4](https://ar5iv.labs.arxiv.org/html/1810.01870#S3.F4 "Figure 4 ‣ III-C Discovering the visual field ‣ III Preliminary applications ‣ Grounding Perception: A Developmental Approach to Sensorimotor Contingencies"). For each motor command Δ​Mq, some sensorimotor transitions have a high probability P​(Xlb|Δ​Mq,Xka). They appear as red diagonals in blocks of the matrix T and capture the fact that the sensory input is shifted between the two corresponding receptive fields during the saccade Δ​Mq. Having estimated this predictive model, the agent can thus predict how sensory inputs ”move” in the visual field when it performs saccades."


### Conclusion

"The framework we develop stands at the intersection of sensorimotor contingencies theory, developmental robotics and predictive modeling."

"Although slightly different algorithms have been proposed to solve each of those problems, they all stem from identical considerations: contingencies imply structure in sensorimotor transformations, and can be captured as such by predictive models."

"Our current effort and main objective is to formalize a single and generic learning framework which would account for the acquisition of any contingency."
* Future aim: unify the three algorithms
* Address problems like ambiguous experiences, hierarchical structures, and compact encoding of contingencies
* They are looking towards incorporating intrinsic motivation and incremental building of hierarchies of contingencies
