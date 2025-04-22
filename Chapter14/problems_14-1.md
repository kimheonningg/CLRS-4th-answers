```plaintext
LONGEST-PATH(G, u, t)
let weights be a new array // weights[i, j] is the max sum of weights from vertex i to vertex j
sort G so that the vertices are in topological order
current_vertex <- u
while current_vertex != t:
    for v in vertices:
        w <- -inf
        if v is next to current_vertex:
            if w < w(v,current_vertex) + weights[u,v]
                w <- w(v,current_vertex) + weights[u,v]
    weights[u, current_vertex] <- w
    current_vertex ++
return weights[u,t]
```

The running time will be O(V+E).
