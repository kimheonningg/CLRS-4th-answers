```plaintext
LONGEST-PALINDROME(str, i, j):
if str.length = 1:
    return 1
if str.length = 2:
    if str[0] = str[1]: return 2
    else return 1

if str[i] = str[j] :
    return LONGEST-PALINDROME(str, i+1, j-1) + 2
else:
    return max {LONGEST-PALINDROME(str, i+1, j), LONGEST-PALINDROME(str, i, j-1)}
```

When implementing with recursion, the recurrence would be T(n) = 2T(n-1) in the worst case. Therefore, the worst case would be T(n)=$2^n$.

```plaintext
LONGEST-PALINDROME(str, i, j):
let dp[0...n, 0...n] be a 2d array with size (n+1)*(n+1)
for i <- 1 to n-1:
    dp[i,i] <- 1
    if str[i] = str[i+1]:
        dp[i,i+1] <- 2
    else
        dp[i,i+1] <- 1
dp[n,n] <- 1

for i <- n-2 downto 1:
    for j <- i+2 to n:
        if x[i] = x[j]:
            dp[i,j] = dp[i+1,j-1] + 2
        else if dp[i+1,j] >= dp[i,j-1]:
            dp[i,j] <- dp[i+1,j]
        else: // dp[i+1,j] < dp[i,j-1]
            dp[i,j] <- dp[i,j-1]
return dp[1,n]
```

When implementing with dynamic programming, it would take O($n^2$) time.
