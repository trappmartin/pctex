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
- Walk `\walk`
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
% Internal nodes
\node[sum] {}; % sum node
\node[prod] {}; % prod node
\node[max] {}; % max node
\node[land] {}; % logic and node
\node[lor] {}; % logic or node

% Leaf nodes
\node[cont] {}; % continuous/gaussian node
\node[bern] {}; % bernouli node
\node[cat] {}; % categorical node

% Generic node style for customization
\node[pcnode] {\large$\top$}; 
```

