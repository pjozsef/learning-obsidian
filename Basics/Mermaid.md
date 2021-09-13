# Mermaid
Use [mermaid.js](https://mermaid-js.github.io/mermaid/#/) to create graphs and other visualizations in your markdown files.

## Usage with Obsidian links
```mermaid
graph TD
a(Basics) --> b(Block Reference)
a(Basics) --> c(Local Graph)
a(Basics) --> d(Query Blocks)
a(Basics) --> e(Mermaid)
class a,b,c,d,e internal-link
```

```
```mermaid
graph TD
a(Basics) --> b(Block Reference)
a(Basics) --> c(Local Graph)
a(Basics) --> d(Query Blocks)
a(Basics) --> e(Mermaid)
class a,b,c,d,e internal-link
```

The trick is `class a,b,c,d,e internal-link`
You need to enumerate your nodes and define them as internal links.

## Getting fancy with nodes and edges
```mermaid
graph TD;
A>looks like a flag] --edge text--> B{diamond shape};
B --thin--> E[square node]
B ==thick==> F(slightly rounded node)
```

```
```mermaid
graph TD;
A>looks like a flag] --edge text--> B{diamond shape};
B --thin--> E[square node]
B ==thick==> F(slightly rounded node)
```