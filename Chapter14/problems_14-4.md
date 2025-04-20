```plaintext
PRINT-NEATLY(l, n, M):
// l: array with word lengths
// n: number of words
// M:maximum num of characters in each line

let extras, lc, c be new arrays
// extras: extra space in each line
// lc[i,j]: cost when words i ~ j is in the same line
// c[j]: min cost when words 1 ~ j are printed

// first initialize extras
for i <- 1 to n:
    extras[i,i] <- M - l[i]
    for j <- i+1 to n:
        extras[i,j] <- extras[i,j-1] - l[j] - 1

//compute lc[i, j]
for i <- 1 to n:
    for j <- 1 to n:
        if extras[i, j] < 0:
            lc[i,j] = inf
        else if j = n and extras[i,j] >= 0:
            lc[i,j] = 0 // end of the paragraph
        else:
            lc[i,j] <- extras[i,j] ^ 3

//compute c[j]
c[0] <- 0
for j <- 1 to n:
    c[j] <- inf
    for i <- 1 to j:
        if c[i-1] + lc[i,j] < c[j]:
            c[j] <- c[i-1] + lc[i,j]

return c[n]
```
