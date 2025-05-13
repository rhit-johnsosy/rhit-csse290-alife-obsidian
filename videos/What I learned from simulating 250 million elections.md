
URL: https://www.youtube.com/watch?v=Jk5Sle7Or1A

![[Pasted image 20250512225135.png]]

Flawed system:
* Plurality voting - 1 person, 1 candidate
	* Known for having more flaws than its peers
	* Ex plurality voting w/ pizzas for a classroom:
	* ![[{749CF998-84C7-476D-BDAB-D14B4CC3D1CC}.png]]
	* ![[{079E12AD-382B-467F-B4E7-2EE05EEC28EE}.png]]
	* 1st group had majority happy and get what they want, while second only a subset were
	* This example also serves as an example of a spoiler effect

Spoiler effect: A situation in which a losing candidate affects the results of an election just by participating.


This student was inspired by this YouTuber and video to look at political science:
![[{FC42ECE2-9F75-4145-8EB7-CA8080718781}.png]]
* might be worth checking out

![[{246A6456-13B6-4656-A952-AA971AA510DA}.png]]


"My question was this, sure election systems have issues, but how bad are they really? How bad can policy get for the population without a bad actor? These are questions impossible to answer through the analysis of history, which is why I decided to simulate democracy."



![[{6ED75023-0995-4E5D-8222-927DD0B54219}.png]]
* Solution: the principle of good enough

![[Pasted image 20250512230239.png]]

Gave example of simple physics 1 cannonball problem and how the result of that is still within tolerance of our actual value.

Even in higher studies of engineering, similar simplifications are used to make problems solvable. 
![[{935F66BE-9737-4E83-ABB8-3215BA6B527A}.png]]


![[{FC60C77F-BED7-4F5B-B6A0-109292430819}.png]]
* "There's a reason that people joke about physicists imagining a spherical cow in a vacuum."
* "If we make no simplifications, then the most efficient way to simulate something is to just do the experiment and let the universe deal with the computation."

Brings up Big-O notation as another example of simplification for the sake of computation.


First step to simplifying democracy:
* Simplifying individual behavior
	* Only care about what decision they make in the voting booth
* System is impossible to simulate from the top down
	* If we already knew how to do this, a simulation wouldn't be needed
* Agent-based modeling
	* Interested in collective behaviors and model them by simulating simplified versions of individual agents which update the state of the simulation.
	* Most famous of these models is Craig Reynold's Boids
		* 3 simple rules to simulate flocking and herding behaviors in animals
		* famous for its use in computer graphics, for films such as Batman Returns and the Lion King
		* has been used for swarm robotics and simulating crowd responses for emergency evacuations 
* taken from political scientists
	* quantify policies and voter preferences as points in a multi-dimensional policy space
		* allows us to treat each individual and policy as vectors
* Utility function

![[{10E1F0B9-FEF2-4B18-8853-8B3BEF1BF26C}.png]]

"If we reframe an election as a type of distributed regression, using a mean squared error actually seems quite natural."
* Chosen bc of conceptual fit, simplicity, and widespread use

How to generate policies that go against our policy?
![[{2AFF526D-089C-4E33-98BC-E1E5A053EE05}.png]]
* Solution: Sample proposals from the same distribution as our population, but scaled by the average distance to the voters.
	* Chosen because
		* Simple to implement
		* Models the tendency of extreme policies to foster the creation of other extreme policies in every direction due to reactionary responses, commonly called the pendulum effect

![[{B60CBFA9-B6AB-4EBF-AB7B-50272FBC3A40}.png]]

* created inefficiency metric
	* a measure of the percentage by which the electoral system is expected to underperform an ideal system

![[{3CB4EC09-EA2C-4525-83A9-105F7E750100}.png]]

* Majority of the interesting behavior happens at the smaller values
* Will space out variables exponentially to balance our runtime and resolution
* To make sure we can detect multivariable relationships we will use a 3D grid


* We can consider the voters to be uniformly distributed around a unit circle, can a draw a circle around each voter to intersect with the optimal policy at the center of the unit circle:
![[{8AAE5149-AB83-4CA6-957C-BBA258D6EB8C}.png]]

![[{9923B388-4C6C-4B08-8DA0-5E2636D1F400}.png]]
* As population increases, inefficiency decreases sharply

![[{FA8CB7BB-27CC-4AF4-8780-9EA30CE0B722}.png]]
* As number of policies increase, inefficiency increases logistically


Illustrative example:
![[{300B0ED7-9B08-4C9E-BFF6-D3D0CF6AFA8A}.png]]
* 5 people one policy leads to a really small area

![[{CD0C5C4E-EE4E-4BA7-BDE4-CC8C82B70C88}.png]]
* 2 new policies can be introduced, that distract 2/5 of the people. This results in a much (9x) larger area, where only 2 votes of the remaining 3 are needed to pass a policy. 

![[{612A834A-A100-4C45-9C22-0D0CC98686AC}.png]]
* If there's a bunch of policies, then what wins is decided by one individual through a tie-breaking procedure

![[{C4F283B1-9EEB-4DBD-8E6D-7BCA5D4DCC73}.png]]
* How the number of dimensions affects inefficiency?
	* Pronounced hump, changes positions based on number of competing policies


For explaining dimensionality, has chosen unit circle and unit sphere as a frame of reference (easy to visualize).

![[{E071DBA3-588F-4A9F-B328-95E40F339365}.png]]
* Ratio is 2D is more than twice that in 3D

![[{DFEB5FEC-DEF9-46D0-9EF3-E49A200A0FD1}.png]]


Wanted to run plurality voting vs a benchmark of no regulation.
* Benchmark picks a random new policy sampled the same way we choose our candidate policies


* Benchmark performed 100s of times worse than plurality voting



"Unfortunately, those in power tend to disenfranchise those who have different political views."



Plurality voting works best when there are only two candidates:
* ![[Pasted image 20250513080032.png]]
* ![[{B7C350A0-E9E2-4D1E-A743-E6FB57AF8C72}.png]]

![[{92E0CD71-0AB8-428E-9654-8591DDA7C94F}.png]]


![[{0D97F48E-1009-4365-BD92-44AB7BF56A15}.png]]

* Important distinction b/t 2 policies on the ballot and a 2 party system


![[{3B0840B9-9F75-496D-9018-175A48885C4E}.png]]
* "In a two-party system, political expression is essentially compressed onto an arbitrary axis between the policies of the two parties."
	* Decreases the dimensions of political expression
		* Increasing inefficiency
	* Axis may not even pass through or even near the optimal policy
	* This could be what leads to the idea of the horseshoe theory
		* ![[{33BB1F37-CC50-4F2C-BD63-8B9C602B0480}.png]]

![[{D9809935-B899-4536-BB3C-38AC71DB08AA}.png]]
* Two party systems are ineffective and potentially even harmful solution to the inadequacies of plurality voting systems. 

Instead of using two party systems to mitigate the problems of plurality voting, instead choose other electoral systems:
![[{E78209FA-4D47-4F7B-B098-1F8B03C8B9C1}.png]]


If we make our decisions off a small number of policy issues, not only are we effectively voting in a smaller dimension, but we may actually be ignoring issues that are important to our well-being. This makes our votes less effective and as a population makes our elections more inefficient. 

