# A summary of: Evolving Neural networks through Augmenting Topologies

[A link to the paper](http://nn.cs.utexas.edu/downloads/papers/stanley.ec02.pdf)

#### What's the point?

 - Evolves a minimal solution by starting with the simplest possible network and adds complexity only when it benefits the solution.

#### Protecting innovation through speciation

When an innovation (new connection or node) is introduced, usually the fitness will drop - a nonlinearity has been introduced where before there was one. In normal systems that compete based on fitness, this genome would die out. The genome needs time to optimise its new structure. In nature, species compete in different niches - the same happens in NEAT. The new genome is protected within its new species. *Explicit fitness sharing* forces individuals with similar genomes to share their fitness payoff.

#### Tracking Genes through Historical Markings

A global innovation number represents the chronology of the appearance of each gene. During crossover, the genes in both genomes with the same innovation number are lined up.
