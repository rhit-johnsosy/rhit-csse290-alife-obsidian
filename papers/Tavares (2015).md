
### Time Taken: 30 minutes

https://wiki.santafe.edu/images/1/12/Sf_csss06_tavares_et_al.pdf



* "Since perceptrons (they aren't linearly separable) are not suitable as a general neuronal component of NCAs, the next logical step is to use a multi-layer feed-forward ANN. The reasoning is straight-forward: it has been proved that networks of this type can learn any function, as long as the hidden layer contains enough neurons." pg. 5
* To evaluate the ANN
	* A test set would be too restrictive and not allow room for complexity and evolution
	* Therefore, measuring complexity is the best way. Score ANNs with higher complexity in their emerging features than those who have less.
* Two different complexity measures mentioned in the article
	* complexity from state changes within each column of the CA matrix
![[{80FDAAC8-3C7C-4F6D-AAC1-C766C7BF7EF3}.png]]
* Kolmogorov complexity for the last row of a given CA matrix
	* complexity in this is defined by the number of bits of the shortest computer program that can be used to fully describe or generate the sequence
	* several algorithms have been made to measure this. Most recent for the paper was Lempel and Ziv's version. Their algo only allows for copy and insert to create the binary sequence.
* These rules can also be used on measuring normal CA, allowing for the comparison between neural CA and normal CA.

* "A novel kind of Cellular Automata was introduced in this work. The common way of representing the set of rules is replaced by an Artificial Neural Network. This provides a biologically inspired automata." pg. 11