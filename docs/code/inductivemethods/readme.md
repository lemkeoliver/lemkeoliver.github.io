## Code related to the paper "Inductive methods for counting number fields", by Brandon Alberts, Robert J. Lemke Oliver, Jiuya Wang, and Melanie Matchett Wood

To view this page in the traditional github tree view, click [here](https://github.com/lemkeoliver/lemkeoliver.github.io/tree/main/docs/code/inductivemethods).

All references below are to the arxiv version of this paper, available here.

### Files

- The file [`SavedDatabase_23_3.mag`](SavedDatabase_23_3.mag) is a Magma file containing the output of the computation described in Section 7.1, which was recorded in Corollary 1.8.
	- More specifically, it contains an array called `Database` of 4953 `GroupCountingInfo` records, corresponding to the 4953 transitive groups of degree up to 23.
	- The `GroupCountingInfo` record is a bespoke record type, whose objects have the following properties:
		- `degree`: The degree of the permutation group
		- `label`: The label of the permutaiton group within its degree, i.e. the group is `TransitiveGroup(degree, label)` in Magma
		- `malleindex`: The Malle index of the group
		- `bound`: The best known exponent in an upper bound for G-extensions that follows from our methods
		- `conjecture`: A boolean indicating whether the number field counting conjecture is known for G-extensions over Q.
		- `isnilpotent`: A boolean indicating whether G is nilpotent
		- `issolvable`: A boolean indicating whether G is solvable
		- `isconcentrated`: A boolean indicating whether G is concentrated.
