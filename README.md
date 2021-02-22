# Hybrid-IDAstar
Does Iterative Deepening A* 2-phase search
 
The Interative Deepening A* is relatively easy to code in 'C' since 
it does not need Queues and Lists to manage memory. Instead the
search space state is held on the LIFO stack frame of recursive
search function calls. Millions of nodes may be created but they
are automatically deleted during backtracking.

Run-time is a disadvantage with complex puzzles. Also it struggles
to solve puzzles with depth g>50. I provided a test puzzle of g=52
that works with ordinary search but the Rosetta challenge puzzle
cycles forever. The HybridIDA solves it in 18 seconds.
 
 The HybridIDA solution has two phases.
1. It stops searching when a permutation begins with 1234.
2. Phase2 begins a regular search with the output of phase 1.

(But an regular one time search can be done with phase 2
only). Phase 1 is optional.)
 
Pros: Hybrid IDA* is faster and solves more puzzles.
Cons: May not find shortest path.
