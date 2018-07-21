Exercise I.

a) O(n)

b) O(log n)

c) O(n * sqrt(n)) => O( sqrt(n))

d) O( (n/2) ^ 2) => O(n^2)

e) O(10n^3) => O(n^3)

f) O(n)
    
g) O(n)

Exercise II

a) a[j] - a[i], where j >= i


  maximumValue = 0
  j = 1
  i = 0
  while j < n:
    i = j - 1
    newValue = a[j] - a[i]
    if newValue > maximumValue:
      maximumValue = newValue
    j += 1
  
b) When we drop the egg there is only two cases the eggs breaks or doesn't break.
So we can drop the egg from the middle of the building floors/2, if the egg breaks then we know we only have floors/2 to test again, this will be our lastFloorTest and we have one egg less. 
Now we can repeat the same test dividing the rest of the remaining floors in half, if the egg didn't break we test on the floor (lastFloorTest + lastFloorTest/2) but if the egg did break then we test on the floor (lastFloorTest - lastFloorTest/2).

Maybe a algorithm similar to a quicksort could solve the problem with O(n log n) complexity

Exercise III

a) Since the pivot is the first element then we still have to go through the whole array to compare his value, then this will be a O(n^2) function and the worst case scenario

b) Since we always chose the median element then we divide the our array in two balanced partitions with size equal to (n/2) or (n-1)/2 each other at each level, so we have a O(log n) funtion per level if we keep doint this for each level up to the last posible level then we have a O(n) * O(log n) or O(n log n) function which will be close to the average.