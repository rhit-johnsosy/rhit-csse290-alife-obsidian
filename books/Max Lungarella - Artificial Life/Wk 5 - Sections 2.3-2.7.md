Chapter 2 focuses on Pattern Formation


### Section 2.3 - Lindenmeyer systems
* pg. 2.14 - Lindenmeyer systems are more intuitively represented in graphics than they are in strings (the strings get very convoluted much faster than the graphics tend to)
	* I wonder if there is a case where the string representation is more intuitive
* Description of turtle graphics pg. 2.15
	* Noticing a lot of overlap with what was covered in the Bio-AI Developmental Systems videos with this section
* "The interpretation of an L-system can be extended to three dimensions by adding a third dimension to the orientation of the turtle" pg. 2.16
* In order to simulate the development of plants
	* More info in production rules
	* Assumption that plants control the important aspects of their own growth. Includes:
		* delay mechanism or influence of environment
		* stochastic element - adds differentiation between plants
* Examples:
![[{0B4F23A5-AF95-4A1B-A93D-6C6A991086D2}.png]]
![[{C611CE54-8CD1-4F8E-B3D9-E8AFD2112724}.png]]


### Section 2.4 - Fractals
* "Fractals are geometric figures that have one striking quality: They are self-similar on multiple scales, which means that a small portion of a fractal often looks similar to the whole object." pg. 2.18
![[{98B9F9F8-C239-4B24-9DBD-42AAFD1BFE42}.png]]

* Fractals often appear in nature. Ex:
	* plants (trees, ferns)
	* snowflakes
	* blood vessels
![[{48FD84AB-592A-4058-87E7-AE2D6288905C}.png]]
![[{20AE7240-B53F-4148-AB8A-35873B8EF88D}.png]]
* "Fractals are nature's answer to hard "optimization" problems" pg. 2.19
	* Ex: supplying every part of the body with blood while minimizing time and resources
	* Additionally the book goes on to make the claim that since blood vessels have been evolved over many years that it is close to an optimal solution. I wonder how we could test that assertion.

* "The trick in generating fractals it come up with a way to describe where and how the miniature version of the whole should be placed." pg. 2.20
	* In general, four types of useful transformations:
		* translation
		* scaling
		* reflection
		* rotation
* Fractal generation algorithms are always recursive and based on self-similarity and they use a combo of those four transformations
	* Ex: Multiple Reduction Copy Machine (MRCM)
![[{23635E0B-9E5E-49D3-A0E4-F5E6F7CBE773}.png]]


### Section 2.5 - Seashells
* Cellular automata can describe the evolution of the colorful patterns of seashells
* Patterns on seashells are made up of calcified material
* Mollusks can only enlarge its shell at the shell margin
* Calcified material and pigmentation process happen at the margin

* process of pattern formation in seashells by activator-inhibitor dynamics
	* cause/suppress pigmentation
	* also called reaction-diffusion dynamics
* "Pattern formation is the result of local self-enhancement (also called autocatalysis) and long-range inhibition."
![[{C8FBAB32-BBEF-43FA-ADA7-49EF2FCA0274}.png]]

* Activator-inhibitor dynamics can be described by
	* Partial differential equations or
	* Cellular automata
![[{FA4D1BB1-2EED-4632-8A4C-66B00BA251BA}.png]]

![[{D7B29DB2-131A-4DC3-9E78-CDEEB20FD2D8}.png]]


### Section 2.6 - Sandpiles
* Self-organized criticality (SOC) came as a result of trying to figure out why nature is so complex and isn't as simple as the laws of physics might imply
* SOC - a mathematical theory of how dissipative systems naturally evolve into a self-organized state with no characteristic to time or length scales
* SOC attempts to explain complex phenomena like
	* distribution of solar flares
	* intensity of sunspots
	* distribution of earthquake sizes
	* size distribution of initial masses of stars
	* distribution of sizes of extinction events

* The sandpile model is a good and easily understandable example of SOC
	* Slowly adding sand to a flat table when it reaches the state where the same number of grains being added are equivalent to the same number of grains falling off the table
![[{C7C51561-238F-4343-BBF1-18DCA5C725E9}.png]]
![[{BA6A94E8-BA0F-4CAF-B105-5105D44CD8E2}.png]]


### Section 2.7 - Conclusion
* "Another central factor in pattern formation is the availability of many cells, and that all the cells are processed in parallel: there must be no central control."