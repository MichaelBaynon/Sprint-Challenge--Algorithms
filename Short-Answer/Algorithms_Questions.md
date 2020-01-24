# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

Obviously I could be wrong but anyway while it does look like there is a decent amount of things going 
on it appears that n doesnt necessarily change rather its just simple math

my assumption is if no value is a re-assigned that helps with the runtime 


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

Most likely wrong again but this one seems a little more complex due to 
the fact that both "j" and "sum" are re-assigned somewhere along the line

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

before I wrote this I believed it was linear just based on appearance since im kind of shooting in the dark but after
noticing the "(bunnies-1)" i am not so sure. I am not even sure that even makes a difference but nonetheless this algo
seems relatively clean and simple thats why I believed it to be a linear

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

 if n = the number of stories 
 and f = the floor at which the eggs begin to break
 
 I assume the point is to be able to throw eggs down and keep them in tact
 also assuming we dont know what F is 
 
 we would start by testing the waters
    we would begin to throw eggs of until we can find F
    once we find F we would basically say you can throw any egg as long as it is below F
    
   maybe in code      if floor < f:
                        throw egg
                      else:
                        go_down_a_floor
                        
 it terms of its runtime class I would have to say it would be either Logarithmic 0(log m) or Linear O(n)
  
