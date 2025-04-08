The Microbial Genetic Algorithm

"Whilst its functionality is effectively similar to the conventional version, it is much easier to program, and recommended for both teaching purposes and practical applications. Despite the simplicity of the core code, it effects Selection, (variable rates of) Recombination, Mutation, Elitism (‘for free’) and Geographical Distribution." pg. 1

"Any system that meets the three basic requirements of Heredity, Variation and Selection will result in evolution." pg. 1

"The most creative and challenging parts of programming a GA are usually the problem-specific aspects. What is the problem space, how can one best design the genotypic expression of potential solutions or phenotypes, and the genotype-phenotype mapping, how should one design an appropriate fitness function to achieve ones goals?" pg. 2

" These are suggestive reasons, but perhaps rather weak, subjective and indeed even aesthetic, for favouring a Steady State version of a GA. A stronger reason for doing so in a minimalist GA is that it can exploit a very simple implementation of selection. " pg. 3

Fitness-proportionate selection
* "regrettably" introduced to newcomers
* " three virtues: it will indeed selectively favour those with higher fitnesses; it has some tenuous connection with the different biological notion of fitness (although in the biological sense any numbers associated with fitness are based on observing, after the event, just how successful an individual was at leaving offspring; as contrasted with the GA approach that reverses cause and effect here); and lastly, it happens to facilitate, for the theoreticians, some mathematical theoremproving. But pragmatically, this method often leads to unnecessary complications." pg. 3
* " What if the chosen evaluation method allocates some fitnesses that are negative? This would not make sense under the biological definition" pg. 3

"by picking two at random, and culling the Loser, or least fit of the two, we have the requisite selection pressure. One can argue that this may be closer to many forms of natural selection in the wild than the former method. " pg. 5

"  Going further, we can consider a yet more unconventional method, that combines the random undirected parent-picking with the directed selection of who is to be culled. Pick two individuals at random to be parents, and generate a new offspring from them; then use the same two individuals for the tournament to select who is culled -- in other words the weaker parent is replaced by the offspring.      It turns out that this is easy to implement, is effective. This is the underlying intuition behind the Microbial GA, so called because we can interpret what is happening here in a different way -- **Evolution without Death!** " pg. 5

"Microbes such as bacteria do not undergo sexual reproduction, but reproduce by binary fission. But they have a further method for exchanging genetic material, bacterial conjugation. Chunks of DNA, plasmids, can be transferred from one bacterium to the next when they are in direct contact with each other." pg. 5

![[{69B5A012-5189-41D4-B738-7B8BB3027004}.png]]
pg. 6

![[{5183DBF5-FBFD-467C-B943-A088593D95B3}.png]]
pg. 7

![[{D2CD6173-FE9E-4D10-8BF9-643D7B08B23C}.png]]
pg. 8
