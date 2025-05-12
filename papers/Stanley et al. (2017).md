
URL: https://www.oreilly.com/radar/open-endedness-the-last-grand-challenge-youve-never-heard-of/


* Open-endedness presented as the last grand challenge 
	* Could be a force for discovering intelligence
	* Or a component of AI itself
* I find the explicit mention of "some beyond the capabilities of all human engineering today" in the following quote interesting as I'd like to think we're capable of a lot more with all of human engineering today, we just haven't assembled it in the right way yet.
	* "Along the way, fantastic inventions, some beyond the capabilities of all of human engineering today, marked the way—photosynthesis, the flight of birds, and human intelligence itself are but a few such triumphs."
* "Evolution better resembles a creative genius unleashed for countless millennia than it does a physical process."
* "open-endedness remains obscure, and interest is confined to a tiny niche of the scientific world"
	* What will make it not obscure?
* "Modern EAs simply don’t keep inventing new things you never imagined in perpetuity."
* "the power of nature is the power of creation, and it’s entirely encapsulated within the mystery of open-endedness"
* "It is now becoming clear that open-endedness, while perhaps simple, involves a kind of mind trick that would force us to reexamine all our assumptions about evolution."
* "**evolution itself is only one** of many possible realizations of **open-endedness**. For example, the human brain seems to exhibit its own open-ended creativity, so it’s likely that an open-ended process can emerge from many different substrates, including within deep learning."

### A brief history of open-endedness
* When researchers build an OEE, they usually aren't looking to solve any specific problem in particular
	* Early examples focused on "artificial worlds" in the hopes of observing a complexity explosion. Ex:
		* Tierra, Avida, Polyworld, Geb, Division Blocks, and Evosphere
* "In the context of open-endedness, novelty search is particularly notable for disentangling open-endedness from any particular “world” or problem domain—it introduces some of the flavor of open-endedness as a generic algorithm that can be applied to almost anything."
	* Allows for directly sorting and comparing based off specific models rather than random
	* "While certainly they mark some progress in our understanding, they are still **missing a key ingredient of open-endedness**—they are destined to stop producing anything interesting within days of launching, and there’s nothing we can do about it. The reason is that their problem domains **contain only a narrow set of possibilities.**"
* Co-evolution is important
	* Example of co-evolutionary-like system that proves useful - GANS (generative adversarial networks)

### The necessary ingredients

* Example set of conditions proposed by Soros and Stanley in 2014
	* **Condition 1:** A rule should be enforced that individuals must meet some minimal criterion (MC) before they can reproduce, and that criterion must be nontrivial. **Corollary**: The initial seed (from which evolution begins) must itself meet the MC and thereby be nontrivial enough to satisfy Condition 1.
	* **Condition 2:** The evolution of new individuals should create novel opportunities for satisfying the MC.
	* **Condition 3:** Decisions about how and where individuals interact with the world should be made by the individuals themselves.
	* **Condition 4:** The potential size and complexity of the individuals’ phenotypes should be (in principle) unbounded.
* Minimal criteria coevolution (MCC)
	* implements the idea of novel individuals creating new opportunities for each other
	* facilitates open-endedness in a generic context independent of any world or domain
	* "The algorithm’s ability to continually generate novel and increasingly complex artifacts is demonstrated through mazes and maze solvers. A population of mazes coevolves with maze navigators controlled by neural networks—the mazes increase in complexity while the neural networks evolve to solve them."
* 