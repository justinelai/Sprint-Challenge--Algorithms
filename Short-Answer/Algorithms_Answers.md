#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)  a = 0
    while (a < n * n * n):
      a = a + n * n

  Total: O(n) - simplifies to rule of multiplication 

 b) sum = 0 
    for i in range(n): 
      j = 1
      while j < n:
        j *= 2
        sum += 1
  
  The inner loop runs log n times for j to be equal to n. The outer loop runs n times.
  Total: O(n*log(n))


c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0            O(1)                      

      return 2 + bunnyEars(bunnies-1)

    Seems tricky because of the recursion. But the size of n does not change.
    Total: O(n)

## Exercise II

This is asking for efficient search, but in vertical form because numbered floors are essentially sorted. 
I would do a binary search, i.e. starting in the middle: number of floors divided by two. Drop egg from that floor. If it breaks, we prioritize the top half of the building. Go to the midpoint of the top half, etc.
Binary search is O(log n)
