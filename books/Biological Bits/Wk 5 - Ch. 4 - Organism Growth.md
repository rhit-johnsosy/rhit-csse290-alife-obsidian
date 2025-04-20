
### Section 1 - Diffusion-limited growth

accretive - characterized by gradual growth or increase

Diffusion-limited accretive growth is different from how a tree slowly expands and creates rings. An example is an agar-coated petri-dish where the starting cell replicates into a structure consisting of branching trees this is because it is best to space out cells to give the most amount of edge space for more access to nutrients.

![[{B1CD826E-2F59-4A1D-9673-4AF6490DB567}.png]]
* Diffusion-limited aggregation (DLA) is a discrete interpretation of diffusion and is easy to simulate algorithmically

Process of aggregation can begin with a single fixed seed in the center of an empty space or a row of fixed seeds along a boundary.
* After this, free-floating particles are introduced creating a "random walk" until they hit a seed and then become attached to and build off the current structure

DLA algorithm simulates the deposition of ions on an electrode.
* It is NOT an accurate model of the development of organisms
* Is a fractal

### Section 2 - Lindenmeyer systems

"Plants are photo-synthesising *autotrophs*; that is, they use energy from the sun to generate their own energy for development and reproduction." pg. 73

![[{215629C3-B57F-45A5-BA22-3A2106011A61}.png]]

L-systems can be used to model plants, tie certain symbols in a string to sticks, stems, leaves, flowers, or fruits.

Axiom: initial string

Production rules: a set of rules that replace a symbol in the string

Turtle graphics - as mentioned in Dr. Yoder's Developmental Systems videos and Lungarella's ALife
* "Imagine a (virtual) turtle roaming a page or screen. The turtle may be instructed to raise or lower its pen, to move ahead a distance, to turn by some amount, to save its position, orientation, and pen conditions by pushing them onto a stack, and to pop this information back off the stack when requested, returning the turtle to a previously stored state." pg. 74-75
* Subroutines can be saved and run repeatedly

### Section 3 - Voxel automata

* Most ways of modelling plants are difficult to include real plant-and-environment interaction as the plant grows
	* Which is a fundamental part of how plants grow in real life

"Ned Greene’s Voxel automata technique (originally called voxel-space automata) closely marries plant development and an environmental model, allowing for some unique plant structures to be grown procedurally" pg. 78
* Has been used to generate complex vines that carpet architecture and respond appropriately to virtual sunlight

Voxel automata naturally account for:
* Phototropic effects that determine the rate and direction of growth
* Growth around obstacles such as rocks, walls, paths and other plants
* Self-intersection avoidance of plant structures

Voxel automata simulations rely on voxels, diced up small cubes of the virtual space.
* Obstacles in the voxels are marked as "filled" in a process called tiling
	* Plants can't grow in these
* Plants grow off of active nodes in accordance with their rules

![[{95ECDF02-B01C-4FFA-94CD-D4FE07BCD237}.png]]
pg. 79
* Selects best segment based on environmental and self-relational conditions
* Heliotropism can even be simulated
	* Heliotropism - the directional growth of a plant in response to sunlight.


### Section 4 - Particle systems

* Everything physical is made up of particles, even if that's not what we first notice when looking at it

Obvious examples of particle systems
* fog
* smoke
* clouds
* sand dunes

Modelling blades of grass. Extendable to other long, flexible plant structures.
* Particles will need
	* size, shape, and color
	* position and velocity vectors
	* birth time and life span
* There also needs to be a particle *generation shape* 
	* Ex: a rectangle flat on the ground for a field of a grass
	* Ex: a single point for producing leaves or fronds drooping in a clump from a branch tip

A generation shape will need:
* A location in space and possibly an extent specified as a line, polygon, or volume.
* A rate at which to generate new particles 
* A start time at which to begin creating particles
* An end time at which to stop creating particles

![[{6C85A8E9-D501-46E7-8257-6F2CD0BF6741}.png]]
pg. 82
repeated until no active particles and no awaiting generation shapes

![[{CF3AC755-1AF6-4CBA-A9B7-B6543B5541D0}.png]]
pg. 82

![[{6EB8880E-26ED-4053-B397-9C2E8B1397B8}.png]]
pg. 83

![[{85BC2A29-9109-4F80-B99E-3BD7963C73EC}.png]]
pg. 84

* Goes into the break-down of substeps in Steps A, B, and C along with those images
	* Worth going back to either replicate grass blades or gain inspiration for another application of particle systems 

