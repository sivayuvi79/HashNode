## DSA-Recurrence Relation

# Recurrence Relation

**Definition of Recurrence: ** Function is calling itself directly or indirectly.

```Python
def fact(n):
  if n==0 or n==1:
    ## o! = 1 and 1! = 1
    return 1
  else:
    return n*fact(n-1)
``` 
There are three type of recurrence relation,
- Substitution Method
- Recursive Tree
- Masters Theorem

## Substitution Method:
  In this method we will be having only one recursive call.

## Recursive Tree:
  If we have more than one recursive call in a script then we call it as Recursive Tree method

## Masters Theorem:
  Actually I missed this class, Surly I will update this as soon as possible



