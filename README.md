# pctex
Collection of useful latex commands for working with probabilistic circuits (PCs).

For general math, see [shortex](https://github.com/trevorcampbell/shortex)

## Commands
### General/Misc

- Log-sum-exp `\lse{i=1}{k}`
- `\poly{N}`
- Independent RVs `X_1 \indepsym X_2` or `\indep{X_1}{X_2}`
- Cond. independent RVs `\cindep{X_1}{X_2}{X_3}`

### General graphs

- Graph `\graph`
- Walk `\walk
- Tree `\tree`
- Vertex set `\vset(\graph)`
- Edge set `\eset(\graph)`
- Node/nodes `\node, \nodes`
- Child/children: `\cnode, \cnodes`
- Children of a node: `\ch{\node}`
- Parents of a node: `\pa{\node}`
- Neighbours: `\neigh{\node}`

### Probabilistic Circuits

- Probabilistic circuit: `\pc`
- Scope function: `\scopesym, \scope{\node}`
- v-tree: `\vtree`
- Sum node/nodes: `\snode, \snodes`
- Product node/nodes: `\pnode, \pnodes`
- Leaf node/nodes: `\lnode, \lnodes`
- Region/regions: `\region, \regions`
- Partition/partitions: `\partition, \partitions`
- Region-graph: `\rg`

### Tikz / Plotting
Plotting is based on an adaptation of `tikzlibraryspn.code.tex` by Nicola Di Mauro and Antonio Vergari.

Reference of provided node type styles:

```
\node[sum]  at (0,1) {}; % sum node
\node[prod] at (1,1) {}; % prod node
\node[max] at (2,1) {}; % max node
\node[land] at (3,1) {}; % logic and node
\node[lor] at (4,1) {}; % logic or node

\node[cont] at (0,0) {}; % continuous/gaussian node
\node[bern] at (1,0) {}; % bernouli node
\node[cat] at (2,0) {}; % categorical node
\node[pcnode] (c) at (3,0) {\large$\top$}; % custom node
```

