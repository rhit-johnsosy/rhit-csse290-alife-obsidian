
### Video 4.1 - Introducing Neural Systems
![[{FA615B43-CAA9-4CC6-AB01-E43CE2AB0A08}.png]]
* habituation - if there is some stimulus that is new initially you might abruptly react to it but if there aren't any negative consequences eventually we learn to ignore it
* paramecium
	* has a mouth (hole) - that allows for material to enter and get broken down
	* cilia - allowing it to move
	* contractile vacuole - regulates how much water is in it

![[{2491028A-A2EE-4488-AE44-FFE13DE8B87E}.png]]
* "If we have the ability to detect information about our environment that gives us a better opportunity to react appropriately in different situations."

![[{496BBF3D-3463-4097-AB87-4979A3CD331A}.png]]
* Types of neurons largely the same between species
* What makes brains different isn't the type of neurons, for the most part, but the amount of them and how they're wired together
	* Similar to the observation in [[Week 5 Reflections - Growth and Development]] about how similar life is between species
* Evolution tends to re-use what's there

![[{21439AF4-743C-4499-98E6-A0DAEFCB2A66}.png]]
* A couple simple ideas:
	* 1. Axon - wire that you can send a signal through, at the end of the axon you will reach the synaptic cleft allowing the sending of neurotransmitters, received by receptor molecules 
	* 2. Dendrites - the receivers of the axon's signals

### Video 4.2 - How Neurons Fire

Notes from the YouTube video played at the beginning:
* Before recent inventions, neuroscientists and scientists at large used squids to study the brain. Specifically, the giant squid axon.
* These days, we know neurons send electrical signals called action potentials using ionic currents and pumps. 
* During the times when scientists couldn't measure action potentials, they used the longfin inshore squid due to the squid's giant axon (1000x wider than a typical human axon). First ever action potential was measured through the squid's giant axon (which was originally mistaken for a blood vessel). 
	* Found the neuron first experiences depolarization (spike) then hyperpolarization (overshoots the normal resting potential). 
		* Added tetrodotoxin (blocks sodium) and tetraethyl-ammonium (blocks potassium) to the axon to figure out the action potential phenomenon. 
				* Found out that sodium channels open first causing depolarization but afterwards potassium channels open causing the hyperpolarization. 

![[{BED82B63-7700-4ADC-A34E-A9D992ED47CB}.png]]
* This model is the product of what was discussed in the YT video
* Has a measurable quantity

![[{22219492-9C28-43E3-9BDF-902FA23F30A8}.png]]

![[{D5CA5316-CE06-4EEE-AAC0-FE6FA6DFF184}.png]]

![[{26248E0E-9264-4D36-8BED-DD8DD09B7602}.png]]
* We have a way to measure the voltage and the change in our current based on the different conditions

![[{113C10F4-EBBB-417D-A8A1-89778F8739E5}.png]]
* There's this process of channels opening and closing
* This model is able to imitate the exact same data that we're doing and all the individual values in the model those correspond with things you actually measure from the system
* A lot of this is possible from being able to study and take down all this data from live organisms

### Video 4.3 - Neuron Communication and Learning

![[{C40AB397-55F3-4D06-857F-BAC962626B50}.png]]
* Whether we choose to talk about how neurons communicate using firing rate or firing time it depends on what we're modelling and what our goals are 

![[{7E8FA57A-8B3A-4817-A96A-330FC63A5D14}.png]]
* Hebb rule - neurons that fire together, wire together
	* Talking about how the amount of time something happens in A leads to something in B reinforces the relationship makes me recall the process of pruning and tuning in the brain by Lisa Feldman Barrett in *7.5 Lessons About the Brain*
* STDP
	* Spike time means that the actual order of one spiking versus the other is important
	* What order are they firing?
	* If they're both spiking at the same time, we shouldn't expect causality. 
	* If we have neuron B firing right after A we would be in the upper-right quadrant
		* If A fires right before B then we want to greatly increase the strength of the connection
		* If we see the opposite occur, then we want to decrease the strength. 
	* LTP - long-term potentiation - for strengthening
	* LTD - long-term depression - for weakening 


### Video 4.4 - Artificial Neural Networks

![[{A0ECA51B-B969-44ED-A1CE-4BED7D62B8E2}.png]]
* Sensory modalities (our 5 senses)
	* Requires special neuron that tells us what's happening in the environment
* Motor neurons are connected to muscles

![[{D8570415-31C7-4333-B45A-61EA9211175E}.png]]
* Basically think of this as taking in some information and outputting some information as a result

![[{5AC5A3C9-F028-4343-AA38-E33B26EE6C91}.png]]
* Pyramidal neurons from biological neurons used as a big inspiration for artificial
* Activation function - used to represent the kind of non-linear transformation that we see with the action potential with the spike
	* Also the notion of a threshold

![[{78F4FA53-74BF-4999-8A01-FC8C2AB2E67D}.png]]
* Generally want something that is non-linear
	* One simple way is the step function
	* Sigmoid function term that I didn't know
		* monotonic - going in one direction (ex: starting low and strictly increasing)

![[{F17E0FDE-0AD8-4D23-AB70-AAC6939A958C}.png]]
* Maybe you need a sufficient number of neurons to fire to figure out what the word is
	* If you try to think of all the things tangentially related to that word, the more different things you can trigger in relation to it, the better the odds of activating the circuit or a neuron that causes a chain reaction that gets you to remember the word

![[{DBBF4291-C651-4466-8A68-79D4D6DC9259}.png]]
* One of the things that we do to simplify the process when we're making ANNs is rather than having each neuron have its own specific threshold, we can have one special node (a bias neuron) that is always sending out a -1 signal. In extension, instead of each neuron having a threshold, we just have a weight to each neuron from the bias unit. 


### Video 4.5 - ANN Encoding and Architectures

![[{09FB9F36-53AD-4559-8FFC-A2CA01D78F8A}.png]]
* grandmother cells - the idea that you have a single neuron that gets activated whenever you have the concept of grandma come up (image, hearing it, etc.) 
* Jennifer Aniston neuron - Jennifer Aniston is a famous actress, popular enough that people tend to know who she is, you can often pick out a single neuron that gets activated whenever people see her that doesn't seem to be activated by anything else
* "we could have memories that are encoded in a way that we end up having neurons be activated related to particular concepts"

* vast majority of the time we have distributed features
	* several different characteristics (ex: round thing, 3D figure)
* re-use of neurons
	* If we have a certain collection of features come together that could be encoding a concept
* a single neuron could have a feature that relates to multiple items
* a single item that has a similar feature that could activate multiple different neurons

* roughly 100 billion neurons in the brain, each of those has roughly 1,000 connections, resulting in about 100 trillion synaptic connections within the brain 


![[{F0E2F6D1-F728-4785-A22F-4FCE87883117}.png]]
* If we have more than 2 layers we call that a deep neural network
* rather than just moving in one direction from the input to the output, we can also put in the idea of a recurrent connection (as seen in example e)
	* having the types of cycling loops within the network it's kind of a way of providing context 
		* if I am always provided the same signals in a feed-forward network I'm going to always produce the same output, this does not hold for recurrent or fully connected networks (can amplify more and more) 
		* the recent past can have an impact on future outputs as opposed to being consistent every the time the same stimulus is presented

![[{DC443207-74A2-4AD6-93E1-74A5D5AB2A6D}.png]]
* Image example
	* First thing we could possibly see are the edges through an edge detector 
		* Put edges together get kind of a shape 
			* Compose shapes together start to get more high-level features
				* Eventually tell if something is a dog or a cat
* By adding hidden layers, makes things deeper
* we can have recurring connections - can think of it as short-term memory - impacts things as that recurrent connection is going 
	* maybe if there's no stimulus for a while then it might kind of die down
* examples of activation functions for ANNs shown in the top-right
	* a lot of times having a smooth, differentiable function will be useful for us
* "a lot of the recent advancements in the last 10 years have not really come out of trying to change anything too drastically with how these artificial networks are set-up but more so the availability of lots of data to be able to train networks on and lots of computing power"
	* more (and better) hardware -> more training
	* more data

![[{6D70D533-6E35-4738-A71D-743E2B47C566}.png]]

![[{5E146C46-EAF5-4455-9494-A072C5363561}.png]]

![[{F6B5B73A-01C1-4480-9F87-C3AA0ECB7499}.png]]
* We tend to re-use and tinker to see what works because we're still struggling to have really great ideas of what architectures work for different problems 

![[{7B88BFA9-8E20-4145-BDAB-58A3373767BC}.png]]


### Video 4.6 - Training Artificial Neural Networks

![[{5E9837C5-84E3-4167-A5B3-252B45CB1F31}.png]]
* Reinforcement learning in psychology - ex: Pavlovian response

![[{8CF12739-088D-4E1A-87FA-60F6A4F82DA6}.png]]
* supervised learning
	* know exactly, based on some input, what we want our output to be
	* use that to train exactly what we want it to move towards
* reinforcement learning
	* we have a reward signal that tells us how good our output was
* unsupervised learning
	* no training or reward signal
	* over time neurons fire together, wire together
		* in the diagram, green signifies that the bond is stronger after nodes 2 and 4 were activated at the same time

![[{E5FC945D-979B-4678-B016-767DD86C3024}.png]]


### Video 4.7 - Unsupervised Learning

![[{DCEE67D6-1206-436C-B939-D65F77DAB74F}.png]]
* strengthen the connection proportional to how much the neurons are firing together
	* in a firing model we can just have a number 0 to 1 per neuron on how active they are 
	* at a particular unit in time, if both are active increase strength, if not don't do anything

![[{05A9B20C-F142-4B5C-9149-9963A9134C0A}.png]]

![[{3E649C7A-46EB-425F-82CD-1D650387B72F}.png]]
* the ratio of the two weights creates a vector out of (0,0)
* same with x

![[{CCEF0812-730F-4BAD-945F-205F2A9F6882}.png]]
* done in ML
* huge amount of data
	* might want to know what gives us the best prediction of something (which particular slice would be the most informative?)
* we can also have a secondary component
* Sanger rules allows for more mathematical guarantee with eigenvectors 

* Ex: 30 dimensions -> 2 would be very helpful


![[{C4DB97B2-2D52-4F4D-B5F8-45B8C9881A5C}.png]]

![[{18A202C7-4306-4057-91C8-D5C7C28D4D2C}.png]]
* Learning the properties of an input set
* If we had a random network and had various weights of the connections and what input patterns they respond to. Initially, probably not much change, but over time with the use of unsupervised learning rules, weights are adjusted to move towards the goal. Ex: the network forming to the purple shape


### Video 4.8 - Supervised Learning

![[{5403B766-395F-4BF6-AB84-900D7EFB08A3}.png]]

![[{CFBAE1E0-8D62-4CF3-B5D5-5F705D60513D}.png]]
* How can we adjust these weights so that we'll be able to correctly determine if a letter is a B or not?

![[{1B4D4EDE-F04D-4DED-9775-00D6C174E3E7}.png]]

![[{75E3864C-0B2A-47D0-8321-C57CF5F1EB96}.png]]
* We can calculate exactly what the error is based on the weights

![[{C4EBC33E-683B-4DA7-B6D7-01CA40D35B12}.png]]

![[{B067B9B9-92EF-493C-A418-31BB8A6D3120}.png]]
* giving ourselves the ability to separate with multiple lines

![[{8B93EBC3-2A20-43E1-A930-A7E2A6F431FB} 1.png]]
* Generally, we need to use a sigmoid function

* We have examples of multilayer feedforward networks being universal approximators

### Video 4.9 - Back-Propagation of Error

![[{98459E84-8698-468E-A294-45E0AD3210C1}.png]]

![[{2DDE5281-2720-4110-9E27-62062AFCE1F0}.png]]

![[{DF2208B0-F2E7-47EC-B98F-D3B4E57D812F}.png]]
* we are trying to look at our based on what our weights are and what kind of error we have, we are trying to move in a direction that minimizes our error


![[{00340B8C-7093-4147-BE44-77EB2F5FA1C4}.png]]
* approximate some kind of function that is mapping out what we care about
* 80-20 train-test split 
* we want the training to occur but we also want to monitor it

![[Pasted image 20250427022630.png]]

![[{90F2AD9B-004A-4E9C-827D-F6A2337618E6}.png]]
* works well in artificial networks, testing out how it works in real life
* 