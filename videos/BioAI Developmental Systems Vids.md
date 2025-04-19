### Video 1. Introducing Developmental Systems
![[{15E12EEF-12ED-4982-AADC-AD8C63837995}.png]]

![[{24F0BD84-B38D-421A-80EB-7388EA7790B6}.png]]
* How do we do this?

![[{FE783237-9990-49C7-919B-0E5D463D0086}.png]]

* Humans have ~23,000 genes
	* A lot less than people were predicting
	* Less than corn
	* Many of our key genes were identical to other animals
	* This was a big shock to many as we were believed to be the most sophisticated and made the assumption that that would require the most genes
	* Therefore, there had to be something beyond genes and mutations that made humans different than the rest
* "The embryo is where the action is in terms of animal diversity. It is the platform diversity"
* "It's not the genes you have but how you use them that generates the great diversity of the animal kingdom." Sean B. Carroll

![[{40131B43-71B5-4EBC-8C01-4BE73B3CCFDF}.png]]

* Can see exact same genes between fruit fly and mouse

![[Pasted image 20250410002822.png]]

![[{8EC44219-9D4F-4566-B362-A6829FBB7708}.png]]
* Precambrian explosion - huge explosion for biodiversity
	* Lot of raw materials before that
	* Used and re-used in many ways
* Hox genes are present in all types of organisms that exist today and those that are extinct

![[{9BE2D5D3-E3DE-40A9-910A-436AD39B7BA2}.png]]

![[{95477236-B1B2-4519-B2B1-581A46FEB904}.png]]

![[Pasted image 20250410003243.png]]
* Allows us to have a very compact encoding
	* Making it easier to search the evolutionary space
* Symmetric and modular structures can be easily defined
	* Don't have to spend time re-defining the cell

### Video 2. Indirect Encoding

![[{68AFBA82-1B4A-4D5F-9647-57A346117E2F}.png]]
* "DNA is more like a program that runs and adjusts things over time"

![[{E661B472-789D-44D9-B0E1-377C71F5CAA9}.png]]
* NEAT serves as a counter-example
* Direct encoding - one gene to one connection
	* Doesn't scale up well

![[{826A04FB-861E-4318-AFF4-FDE672078D0E}.png]]

![[{9412D466-3FCD-499D-B9A5-C1B8C4C1E203}.png]]
* Serves as an example of how simple physics and chemical rules can cause something complex to develop through emergence

### Video 3. Rewriting Systems Intro to L-Systems

![[{A02DA588-2CE4-42FE-B307-9CEEDF6960CD}.png]]
* Generator appears on flat edges recursively, resulting in a more complex shape (snowflake)
* Nice visual representation for representing a complex structure compactly

![[{5C76C320-14C2-413F-814D-BF9678DF0112}.png]]

![[{B262E412-CD28-4429-BEFC-B9A40722C0C7}.png]]

![[{1857114D-EA50-46D9-BF4B-169D323D8C9B}.png]]
* Grows based on defined rules
* Similar to cellular automata

![[{075B1395-639F-47E1-A75F-2C6221967586}.png]]
* "Our goal is to see how a re-writing rule with a simple number of instructions can generate something that's pretty complex."

![[{23409B20-E699-4CB4-AF90-7CA3C49AE234}.png]]

![[{D9E3E846-EF77-47B9-B5FC-8FDE236553FB}.png]]

![[{5D917985-7240-49F9-B08D-B89780F6C5D4}.png]]
* Interprets the string as a set of movement commands like forward, turn right, turn left, etc.

![[{3C6E5EEF-26AE-41B0-A5AC-76F554922E3A}.png]]
* The numbers in the example string are how far we should skip
* We can use this to define any kind of network we want including neural networks
* 2 steps
	* 1. Generate string
	* 2. Interpret string

### Video 6.4 Advanced L-Systems
![[{D90F7039-4D9C-474B-B0E6-A0FD3AE21167}.png]]
* "Rather than having to backtrack we can have a couple different symbols"
	* These symbols allow us to save and go back to certain spots - kind of like github
	* Saving the current state of the turtle and putting it on a stack
* Kind of hard to see in the image but the open bracket is the save and the close bracket is the restore

![[{D2E3F99B-200C-42EA-A881-6D37CBD740BC}.png]]
* Instead of just a fractal pattern we can have a fern pattern
	* Given that we have a fern pattern that seems a lot closer to how us humans see life, I wonder how close we are to having algorithms recreate things we typically view as life on their own
* In a deterministic system, we will always get the same result
	* To change this that's when we add noise or stochasticity

![[{B281CBCD-B825-46BB-B298-AF3D03B047A9}.png]]

![[{3DDCDFAD-2F8F-462A-AC57-60567E4BC258}.png]]
* Example elaboration: "a can get translated to g assuming there's a b on its left and a c on its right"
* Context-sensitive bracket allows us to add more stuff while maintaining the original rule, allows us to rewrite or adjust

![[{3E550336-6E5C-429D-95AD-8B99B56DE690}.png]]

![[{D87DD0B2-497F-4DEF-9342-FE38EF9CBD99}.png]]

![[{45FB567A-3432-4488-B5AD-0485BD0C09BC}.png]]
* "If we want to generate a scene but not have to define all the different pieces of a particular tree but have things that look nice this is a great way to do it."

![[{C30CEBAA-D13A-47E5-975A-164582C60D04}.png]]

From the video's quiz:
* Bracketed L-Systems make it easier to represent hierarchical structures
* Context sensitive L-Systems allow for a means to propagate signals across a structure that cannot be done with context-free L-Systems
* Context sensitive L-Systems have an analogy to cells that might be responsive to different local concentrations of chemicals or hormones

### Video 6.5 - Synthesis of Developmental Systems
![[{67395F96-68E1-4565-8EA8-7AC847BAF1D7}.png]]
* Example of inverse problem: trying to get cellular automata to do a specific thing (have a specific outcome)

![[{E9BC5724-F6E5-4442-8A59-A87824BB5A7E}.png]]

![[{841FF7E4-6176-4C2F-9754-DC100D24E139}.png]]
* Matrices!!!
	* I am currently taking MA371 - Linear Algebra and CSSE/MA415 - Machine Learning and I found that a certain lesson and HW assignment seemed to be directly taking content from linear algebra to fuse it into ML. I wonder how much linear algebra is a part of Bio-AI and ALife.
* Allows for compactly storing a bunch of info

![[{907F7F4F-904F-4C14-B8B7-2D7F6B7E3347}.png]]
* Compared to matrix rewriting, direct encoding requires a lot more storage of info

![[{A22CA857-5299-4FCE-84AF-A9AD4D619D8B}.png]]

Correct Answers from the Quiz (good review):
* Rewriting rules can sometimes be deduced from understanding of a developmental process
* The inverse problem refers to trying to determine the rules for a rewriting system in order to produce a specific final outcome
* Evolution can be used to synthesize developmental systems
* Some indirect encoding schemes for neural network structure have been shown to scale better to larger problems than a direct encoding

### Video 6.6 - Cellular Encoding

![[{FCD4ED74-4653-4320-8171-0F4AE158C311}.png]]
* Dr. Yoder mentions that we're going to do something similar to HW2 with genetic programming but I haven't taken Bio-AI (What was HW2?)

![[{238FA83F-E428-4977-8FDB-D88B22B35BAA}.png]]
![[{B28AC929-7C5D-40AF-B808-130BEFBEE52C}.png]]

![[{BA32F6B9-2692-44E1-8AAA-78F08647AAD5}.png]]
* Single tree is complicated and pretty large
* Multiple trees allows us to re-use multiple components making the result a lot less complicated

Correct Quiz Answers:
* Cellular encoding makes it possible to have a network grow from a single mother cell
* Gruau evolved a tree structure to be read as instructions for how to update a network of connected cells over time


### Video 6.7 - Artificial Ontogeny

![[{579D904D-11F5-42C1-B55F-9BA79B920A58}.png]]

![[{371D2A26-59EC-4213-8917-5AA5C6057BA6}.png]]
* Purpose of example: "Can we get something that will grow out and push a block?"
* From the 2000s


Further simulation of example:
![[{7539B215-1A29-4D13-87D5-5F748CB3EC60}.png]]
![[{88AA745D-97A1-4446-AFE6-04854E5BEB5D}.png]]
![[{BF9C668F-3429-418F-AF1E-0F61C4A691F5}.png]]

![[{9F6558FD-0C6A-48F4-809C-01350DD3CFA6}.png]]
* Some cells die off

![[{8332B3CC-7000-40E5-BF9C-4B3CDA1C482E}.png]]
* Eventually does stop growing in place and moves to try and tilt over the box (to not much success)


![[{8D8A4FB7-A219-4CA1-A094-A425A8DCCFC8}.png]]
* "Could we make an artificial developmental system that could allow us to have a compact genetic encoding that produces complex structures and makes it more efficient for us to be able to go and find things that could work?"
* With the heavy cross-over of CS and Biology, especially in that last simulation, it would be interesting to know if Dr. Robert Williamson has had any success tackling the box example or some other Bio-AI application due to his in-depth knowledge of both fields.

Correct Quiz Answers:
* the multicellular creatures are equivalent to cellular automata
* cells have a genome which is expressed based on various input signals and states







### Video 6.8 - Compositional Pattern Producing Networks

![[{A439355A-7452-4AB3-8F5D-05078E153E8E}.png]]
* A network that represent an abstraction of development
* "Abstraction because we aren't having anything unfolding over time"

![[{929053C2-8A4B-4212-AA8E-F6EBF0FEEB87}.png]]

![[{2B301084-EB76-44B0-A31B-5AADF97961E0}.png]]
* "Just like how we have seen the way that a gradient of chemicals might fall from one end of the body to other and that's used to differentiate body parts." -- patterns can do the same

![[{7FCBA2F1-9A87-4956-95F8-862C6E6E87AC}.png]]
![[{245E9605-D2D4-43CE-9C90-00BE000391DE}.png]]

![[{A0C07429-BDE1-4090-95CE-9AFB4BE0B8DD}.png]]
![[{82E22047-0EF6-4279-9EA4-B2B958B4E7E7}.png]]


![[{E9489A40-D219-4727-8107-A8D114A9BFCF}.png]]
* Original goal: "Can we produce patterns that look like developmental patterns?"
* To enhance the things we can build we can add
	* Not just x, y
	* But also a bias
	* And a distance (i.e. from the center)

![[{2D433139-DB1E-46E7-9AC7-CE07594462DC}.png]]

![[{C9B97EF4-3597-41B9-BD21-6169D50F2A73}.png]]
* We can use this to create something we find interesting like a spaceship-like image
* And then further evolve it (see img below)
![[{1B75F2FB-32D6-40E7-A582-517667F3E6AD}.png]]

![[{9E044D8D-07EB-4252-A92B-32F76124BF54}.png]]
* We may have a gene that only modifies things slightly

![[{0D4A7C19-1531-4150-AD06-8AF86AE26740}.png]]
* Another example

![[{D80FA770-6817-4AEF-9D8A-8E089D7A6B87}.png]]
* Another example
* Passing in sin(x) instead of just x
	* Allows us to create patterns that are periodic

![[{91BED88A-63EC-4534-9440-739DDCA46EB4}.png]]

Correct Quiz Answers:
* CPPNs produce visual patterns which can then be selected by humans as appearing lifelike or interesting or not
* CPPNs are extremely efficient compared to other approaches of mapping a genotype to a phenotype 
* CPPNs manage to capture relationships to what might be analogous to different stages in a developmental process
* Examples of kinds of input features that may be used in a CPPN
	* x coordinate
	* y coordinate
	* distance from center
	* sin(x)





### Video 6.9 - HyperNEAT

![[{05F3081D-0D56-478A-9373-3CEBB0ACC187}.png]]
* 16 hour timelapse of a zebra fish
* "Its brain is growing in front of your eyes."

![[{80896682-C7BD-4301-BD6D-6C7013D7FAA2}.png]]
* "Little neurons branch out and find connections and build a part of the brain of this zebra fish"
* Won some awards
* Is NOT a simulation, is a video watching it actually occur

![[{3C30B625-0156-4883-87C9-0AD28CD9A758}.png]]
* "We can see lots of cells moving around and that one connection going across the screen"


![[{4C896054-CFBD-4D14-A359-3860D4DEB39C}.png]]
* "HyperNEAT is going to be an approach to using that CPPN to determine what parts of a neural network are connected to what other parts in a very impressive and powerful fashion."
* A pattern producing network, based on what we put into it, give us out an image.

![[{AEDFBD89-89AE-49EE-98CA-D5B62699E4E8}.png]]
* Take in 4 different parameters (in this example)
	* 2 x's, 2 y's
	* Pick a specific spot set x2 and y2 to that spot (ex: (-1,-1)). Those will be fixed values
	* Pass in x1 and y1 as all the coordinates from a given space (ex: the whole target matrix/board)
	* Further elaborated in the slide marked up right below
![[{8D8883C9-AFE1-4E9F-905F-718B6727F393}.png]]
* Black space shows connection, white/blank shows the absence of

![[{1E9507C5-79EA-4C46-A26E-CFBBA63D9BBE}.png]]
* "Each neuron effectively has a pattern that decides what it's connected to."
* "We have a square, we have a cube, then we go one dimension higher and then it's a hyper-cube."
* "The geometry of how things are actually laid out could be a really big deal in helping us solve the problem."
* "A way for us to again have a single network that determines ALL the different connections AND it's doing it at scale."


![[{820E14E0-66A2-49AC-AA43-0B64104F3F10}.png]]
* Using this method, break things in quadrants
* "We now have a way to scale up a neural network to arbitrary dimensions" (# of nodes)

Correct Quiz Answers:
* HyperNEAT is an example of an indirect encoding for a neural network's weights
* HyperNEAT utilizes a CPPN with at least 4 inputs to determine how strongly neurons are connected to other neurons
* A CPPN with four inputs which is provided two fixed values results in a 2D pattern being produced
* HyperNEAT can be used to train neural network with millions of nodes
* There have been many extensions to HyperNEAT including a version that allows the network to efficiently remove redundant nodes and 
