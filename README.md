# deep_reasoning
A novel approach to create an AI tool that can achieve two main goals - capable of reasoning more reliably and generate new ideas to solve truly new problems.


# Idea: Understanding, Reasoning, Creativity are achieved via Analogy [Work in Progress]

The proposed concept rests on the premise that both reasoning and creativity are forms of analogy finding. Reasoning, particularly evident in mathematical truths, involves applying known rules to new entities.

Creativity, on the other hand, can be viewed as analogy finding with relaxed constraints. It allows for the application of known patterns in one domain to another, often breaking some existing rules. This violation of rules or assumptions leads to innovative thinking and novel solutions, although not all creative ideas will be valid or useful.

Both reasoning and creativity uses analogy as the underlying common process to create and validate new and existing ideas. Finding analogy can be translated into a well known problem in Graph Theory - called Graph Isomorphism. If we map concepts to nodes and relationship among concepts as edges, we can transform a piece of fact or knowledge into a graph. Although this is not a new approach, the idea of using graph isomorphism to detect patterns of reasoning is new. 

Converting text or input training data into graphs will be the first major task for this project. We will also need an effcient algorithm to find isomorphism. These graphs will be represented via set of embedding vectors in a continuous vector space, instead of the traditional discrete nodes and edge based graphs.

# Architecture, Core Algorithm

The system will comprise two principal components: a persistent memory and a set of processes dedicated to editing this memory.

At its core, the memory is structured similarly to a graph. Within this graph, a 'graphlet' is defined as a connected subset comprising specific nodes and edges.

Each graphlet embodies a distinct piece of knowledge. This knowledge might represent either a direct fact about the world or a learned pattern. Interestingly, a single node within this structure has the potential to represent an entire graphlet. Some graphlets serve a unique function: they symbolize relationships between other graphlets by referring to them as nodes. These relational graphlets are instrumental in transforming one graphlet into another, akin to a logical deduction process.

When graphlets can be derived from one another, they collectively form what is known as an 'equivalence set'. This relationship is represented through a directed graph. For instance, if there are two graphlets, A and B, and each can be deduced from the other, we define a 'morph' as the set of changes required to transform one graphlet into the other. In essence, learning logic in this context involves mastering these morph functions.

Reasoning within this system can occur in two primary ways. Firstly, we can map a given graphlet to another through the process of graph isomorphism. Alternatively, a graphlet can be transformed into a new one using one or more of the known morphs.

