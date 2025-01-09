---
title: "Announcing PHART!"
date: 2024-12-29
---

## Features
- Pure Python implementation
- Render using 7-bit ASCII or unicode characters
- No external dependencies (except NetworkX)
- Multiple node styles (square, round, diamond)
- Customizable edge characters
- Support for directed and undirected graphs
- Handles cycles and complex layouts
- Bidirectional edge support
- NetworkX graphs, DOT, or GraphML input
- CLI will even accept a .py file as input for changing/testing options without editing scripts
- lots of examples in the repo
  
### Python API Example:
```python
import networkx as nx
from phart import ASCIIRenderer

# Create a simple graph
G = nx.DiGraph()
G.add_edges_from([("A", "B"), ("A", "C"), ("B", "D")])

# Render it in ASCII
renderer = ASCIIRenderer(G)
print(renderer.render())

     [A]
      │
   v  │   v
  [B]────[C]
   │
   │  v
   ──[D]
```

### CLI example:
```bash
# Using Unicode (default)
phart graph.dot
# ┌─A─┐
# │   │
# └─B─┘

# Using ASCII only
phart --charset ascii graph.dot
# +-A-+
# |   |
# +-B-+
```
----
[phart@github](https://github.com/scottvr/phart)
[phart@PyPi](https://pypi.org/project/phart/) or `pip install phart`


Announcing [PHART - the Python Heirarchichal ASCII Renderer Tool](https://github.com/scottvr/phart)
