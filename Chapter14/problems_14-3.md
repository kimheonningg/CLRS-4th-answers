```plaintext
BITONIC-TOURS(p):
sort p so that the x coordinate of p[1], p[2], ... p[n] are ascending
let b be new arrays
b[1,2] <- distanceOf(p[1], p[2])
for j <- 3 to n:
    for i <- 1 to j-2: // j-1 is handled afterwards
        b[i,j] <- b[i,j-1] + distanceOf(p[j-1], p[j])
    b[j-1, j] <- inf
    for k <- 1 to j-2: // for every combinations
        q <- b[k,j-1] + distanceOf(p[k], p[j])
        if q < b[j-1,j]
            b[j-1,j] <- q // update min value
b[n,n] <- b[n-1,n] + distanceOf(p[n-1], p[n])
```
