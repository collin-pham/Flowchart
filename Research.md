# A compilation of research I've done for this project and the roadmap for implementation. 

> Serves to communicate my thought processes and design decisions

## Initial Thoughts & Understanding of the Problem

> Design a flow chart application that can take variables and increment, decrement, multiply, divide and/or apply conditional operations to them. We are designing this system for a user who has never written code before. It should be intuative and simple.

A flowchart is a non-directed graph, thus each node in the graph will represent:
1. A variable decleration
1. An arithmetic operation on a variable
1. A condition
1. A result

Each edge will represent a relationship/transfer of information between each node. Thus, there must be constraints on the number of edges specific nodes can have ( a arithmetic node should only two edges ).

### Logic of flowchart layout

The most simple scripts run synchronously. Our flowchart should mimic this execution. 

Our flowchart will have a "genesis block", after which will follow any variable decleration, operations or conditions.

      
[Genesis Block] -> [Declare (var a = 5)] -> [Multiply (5 by a)] -> [ Result ]

Questions for Wednesday:

1. How should the "result" be handled / display information? 
1. Can more logic happen after a result block, or is this the end. 
1. What conditional logic should be implemented?

## Potential Libraries

1. jsPlumb
1. jointJS
1. GoJS

### jsPlumb

Seems a bit too powerful for what we are trying to build. It does have an AST visualizer that can implement functions, returns, etc. Further, the suggested layout for code mimicry does not seem intuative to me, suggesting it won't seem intuative to a user who has never written code before.

### jointJS

Simple Flowchart builder with underlying JSON structure. Supports React. Looks like it has good documentation. Seems to be customizable. Leaning towards this library. 


### GoJS

Similar to jointJS, but does not have tutorial for React. 






