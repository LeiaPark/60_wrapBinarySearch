# exercise the List.indexOf

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

# hw60

What is meant by y = log2x?
  
> The equation seeks to determine how many times 2 must multiply by itself to equal the value "x". The number of times is represented by the value "y".

What does its graph look like?

> The graph can be seen in the [fourth edition of Cohen's Precalculus with Unit Circle Trigonometry](http://davidmholmes.net/Stuy/ap/hw/logarithms.pdf)

### Recursive Solution Description

0. Decision-making: The low limit is less than or equal to the high limit.
1. Solution to base case: Return -1, which means the element wasn’t found
2. Solution to recursive case:
> If the value at the middle index is equal to the value we are looking for

>     Return that middle index

> If the value we are looking for is less than the value at the middle index

>     Set the new high value to the middle index - 1
>     Call this function again with the new high value and same low value

> Else

>     Set the new low value to the middle index + 1
>     Call this function again with the new low value and same high value
