#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) The basic logic this algorithm is getting to, is at what point does n^2 get greater than or equal to than n^3. (How many n^2 can you fit into n^3). n^3 / n^2 = n, so therefore the time complexity of this algorithm is O(n).
 

b) Run time of this algorithm is O(n log(n)), as the for loop is O(n), but the while loop inside that is dependent on variable j is increasing at a rate of 2^j, which equates to a time complexity of log(n). Since the while loop is nested inside the for, you have to multiply n * log(n)


c) Run time of this algorithm is O(n) (or O(bunnies)). As n increases, so does the amount of times recursion on the algorithm happens, as the recursive argument is n-1, and the stopping condition is when n = 0. 

## Exercise II


Start by throwing an egg from the middle floor of the building (n/2)
    If it breaks, try throwing an egg from the middle of the lower half of the building height that was just checked (for the first pass, take the middle of floor 0 and the floor num you just previously tried throwing the egg from)

    If it doesn't break, try throwing an egg from the middle of the upper half of the building height that was just checked (for the first pass, take the middle of the floor num you just previously tried throwing the egg from, and the top floor num)

Continue this cycle until there are 2 floors left, and at this point, the upper half floor should break, and the lower should not. 

This is a form of binary search to go about this problem, and therefore the time complexity would be O(log n)