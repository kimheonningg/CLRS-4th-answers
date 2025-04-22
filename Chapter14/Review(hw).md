Items we have learned so afr up to DP
space complexity no


10 Sorting algorithm.
    n^2
    nlogn
    n
Algorithm to solve selection problem


Running time analysis.
    usually worst and average case.

    Asymptotic analyses.
        Big-O, theta(usually use this!)
    
    How to compute running time.
        # of for/while.
        function call.
        line.
    
    Most informative. thetha.


    (10pt) What it the asymptotic of below?


Divide and conquer.
    if we have optimal sub- then we can get the optimal solution via di and q

    recurrence. 
        recursive.
        related to divide and conquer.
    
    method to solve recurrences.
        substitution method
            good suppose 
        Recursion tree method. => 이거 그리는거 나오려나?
            draw tree.
        Master method.
            the equation ts fit to the form.
        (NO) akrabazzi

    
Sorting algorithms
    1. 
        Selection sort. 
            find max and swap
        Bubble
            basically on same Idea with selection. 
            find max on 2.
        Insertion sort.
            find inorder and move until the correct position

    2. 
        Merge sort
            divide into 2 groups. and then merge

        quick pica a pivot element.
            mostly use because this is fast.
            Quick sort inside the subarray.
            get the right position of pivot.
        
        Heap sort.
            use special structure.
            max obtain in nlog n for 

        Shell sort.
            doing insertion sort with slide. 
    
    3. 
        Counting sort. 
            Big data 
            huge space complexity.

        Radix sort
            similar with counting.
            sort with digits.
            => what if call Radix sort for a digit.
        
        Bucket sort.


Selection.
    ith order statistic.
    1. minimum and maximum find.(Easiest. but takes long time complexity)
        => scan 1
        at least have i array/
    
    Sort for ith is not good

    2. with heap.

    3. linear select => 엄청 열심히 설명하시니 시험에 무조건 나올 듯.
        best case sinario in quick sort.
        worst/always cost 분석.

        don't need to sort all the element.
    
DP.
    1. optimal substructure.
    2. Overlapping recursive calls.
    => DP is solution

    #1. paths in matrix
    #2. Placing stones(pebbel) 뭔가 더 설명함.
        DP with memoization. 
    #3. Matrix Chain Multiplication. C(i, j) = min(C(i, k))

    #4. LCS
    #5. OBST

    memoization.


Running time analysis => merged 
ith order statistics => more tricks we can speed up
