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

Example plot in example.pdf:

```
\begin{tikzpicture}

\sumnode{s1};
\prodnode[below=15pt of s1, xshift=30pt]{p1};
\prodnode[below=15pt of s1, xshift=-30pt]{p2};

\bernode[below=15pt of p1, xshift=-15pt]{v1}{$X_0$};
\bernode[below=15pt of p2, xshift=15pt]{v2}{$\bar{X}_0$};
	
\contnode[below=15pt of p1, xshift=15pt]{v3}{$X_1$};
\contnode[below=15pt of p2, xshift=-15pt]{v4}{$X_1$};
	
\weigedge[right] {s1} {p1} {$\theta_1$};
\weigedge[left] {s1} {p2} {$\theta_2$};

\edge {p1} {v1};
\edge {p2} {v2};
\edge {p1} {v3};
\edge {p2} {v4};
\end{tikzpicture}
```

