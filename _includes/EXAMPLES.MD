---

---

## PHART Graph Visualization Examples

=================================

### In preparation for a 1.0 PyPi release

I was doing some last-minute testing and came across this, from the networkx gallery:

https://networkx.org/documentation/latest/auto_examples/drawing/plot_chess_masters.html#sphx-glr-auto-examples-drawing-plot-chess-masters-py

The code there creates a graph from some data pulled from a database of Chess masters tournaments and such at this site:

https://chessproblem.my-free-games.com/chess/games/Download-PGN.php

And plots it with matplotlib. It looked pretty complex so I thought as a lark I would see how difficult it would be to get phart to render the graph. The matplot can be seen here:

![screen capture of graph plot](https://github.com/scottvr/phart/blob/67bd3d02b6ad9cc4a8a09fe6fc2920a6712f5c7a/examples/WCC-plt-Capture.png)

So, I added the following to the code at the networkx gallery page linked above:

```
from phart import ASCIIRenderer, NodeStyle

.. existing code remains here ...

... then directly below the existing lines to create the nx graph:
# make new undirected graph H without multi-edges
H = nx.Graph(G)
... I added this:
renderer=ASCIIRenderer(H)
renderer.write_to_file("wcc.txt")
```

and ran the code. Immediately this was written to wcc.txt:

```
                               ---------------------------------[Botvinnik, Mikhail M]---------------------------------
                               |               |                           |                 |                        |
            v                  |               |                    v      |                 |                        |                     v
  [Bronstein, David I]----[Euwe, Max]----[Keres, Paul]----[Petrosian, Tigran V]----[Reshevsky, Samuel H]----[Smyslov, Vassily V]----[Tal, Mikhail N]
                               ^                               |    |
                                                               |    |                   v
                                                    [Alekhine, Alexander A]----[Spassky, Boris V]
                                                               |           |            |
                                                  v            |           |            |           v
                                        [Bogoljubow, Efim D]----[Capablanca, Jose Raul] ---[Fischer, Robert J]
                                                                          |^
                                                                          |
                                                                  [Lasker, Emanuel]--------------
                                                                          |                     |
                            v                      v                      v                     |                       v
                   [Janowski, Dawid M]----[Marshall, Frank J]----[Schlechter, Carl]----[Steinitz, Wilhelm]----[Tarrasch, Siegbert]
                                                                                                |  |
                                                 v                        v                     |  |
                                       [Chigorin, Mikhail I]----[Gunsberg, Isidor A]----[Zukertort, Johannes H]


                                            [Karpov, Anatoly]----[Kasparov, Gary]----[Korchnoi, Viktor L]
```

No fuss. No muss. Just phart.

### Software Dependency Example:

```
            [main.py]
                |
         v      |       v
    [config.py]----[utils.py]
         |              |
         v              | v
  [constants.py]----[helpers.py]
```

### Organizational Hierarchy Example:

```
                                       [CEO]
                                         |
                                v        v        v
                              [CFO]----[COO]----[CTO]
                                |        |        |
        v              v        |      v |        |       v                v
  [Controller]----[Dev Lead]----[Marketing Dir]----[Research Lead]----[Sales Dir]
```

### Network Topology Example:

```
                     [Router1]
                         |
                   v     |      v
               [Switch1]----[Switch2]
                   |            |
      v            v            |            v
  [Server1]----[Server2]    [Server3]----[Server4]
```

### Workflow Example:

```
        [Start]
           |
           v
        [Input]
           |
           |v
       [Validate]
            |
           v|
     --[Process]
     |     ^
     |     v
     |  [Check]
     |     |
     |     |     v
  [Error]----[Success]
                 |
            v    |
        [Output]--
            |
           v|
         [End]
```

### DOT Import Example:

```
     [A]
      |
   v  |   v
  [B]----[D]
   |      |
   |  v   |
   --[C]---
      |
      v
     [E]
```

## Custom Styling Example:

Different node styles for the same graph:

### Using MINIMAL style:

```
         0
         |
       v |  v
       1----2
       |    |
  v    v    |    v
  3----4    5----6
```

### Using SQUARE style:

```
            [0]
             |
          v  |   v
         [1]----[2]
          |      |
   v      v      |      v
  [3]----[4]    [5]----[6]
```

### Using ROUND style:

```
            (0)
             |
          v  |   v
         (1)----(2)
          |      |
   v      v      |      v
  (3)----(4)    (5)----(6)
```

### Using DIAMOND style:

```
            <0>
             |
          v  |   v
         <1>----<2>
          |      |
   v      v      |      v
  <3>----<4>    <5>----<6>
```
