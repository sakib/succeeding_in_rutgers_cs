# Systematic Interview Process

I like lists so I made this and whenever I did a mock interview with someone, I used this as a reference until it became ingrained in the way I do interviews. It helps a lot.

1. Ask intelligent clarifying questions: for *this* input, do I get *this* output? Your goal should be to really understand the problem.

2. Build your set of 2-3 *comprehensive* test cases. Consider edge cases out loud and how to handle them. Write the cases out so you don't forget.

3. Now that you know your program's desired behavior, sketch out 2-4 algorithms to solve the problem. Always start with the dumbest brute-force algorithm and gradually improve on it by recognizing places you're wasting computation. Brainstorm things you know like dynamic programming, visualizing the problem as a graph/tree, etc. In the worst case, you have 1 dumb, brute-force algorithm that you can technically implement.

4. For each of your 2-4 algorithms, list next to them their expected time and space complexities. Optionally, note their simplicity/readability as well. Make sure to list out all relevant parameters before you say anything like "this is O(N)!"

  | Algo |   Time   | Space  | Simple? |
  | ---- | -------- | ------ | ------- |
  |   1  |  O(n^2)  | O(1)   |  yes    |
  |   2  |   O(n)   | O(n)   |  maybe  |
  |   3  | O(log n) | O(n^2) |  eh?    |

5. Compare and contrast the algorithms out loud, taking into consideration all of the parameters you've laid out. Consider: code length, time limitations, system capabilities (what's the I/O bandwidth?), and your own ability/confidence in writing out the solutions in full. If you expect you won't have enough time to finish one solution, ask if it's okay to modularize some functionality out and finish later if you have time once you finish the main algorithm. Only commit to one approach after consulting your interviewer for their preference (if they have any).

6. Important: sketch out exactly how exactly you're going to implement your chosen solution. Anticipate what methods you're going to need, their signatures, runtimes and input/outputs. This is better than getting deep into your solution and realizing that one code segment is better off being modularized for cleanliness/usability, or realizing that another solution is better entirely. Example: Given a binary tree, print out all paths that sum to a given target value.
You might think to use BFS here, but DFS is better because then you can just print out the values of the nodes when your recursion propagates back ui rather than keeping auxiliary data structures to track your paths.

7. Start implementing your solution in code. Don't make them ask you to do this. This should be ~5 minutes into the interview now. If one segment of code is going to take a significant chunk of time and isn't part of your main algorithm, offload it to another method, assume it'll work and tell interviewer you'll implement it later if you have time, then continue. Your main algorithm is the main priority.

8. If you get to this point, immediately run your algorithm on 1-2 of your test cases. There's no need to run line-by-line, just make sure it works - it's great if you catch your own mistakes here, so that the interviewer sees that you're self-righting.

9. Ideally by this point, your code is clean, modularized and ready-to-run. But if it's not, scan it now for readability, runtime, etc. and speak your thoughts.

10. The interviewer should be satisfied now and will probably take a picture of your work.
