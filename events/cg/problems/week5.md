## Week 5 

Write down a function that takes an N x N matrix as its argument (you can assume that a square matrix is passed to the function, you don’t need to check for it). The function should return a new matrix B such that B[i,j] is the sum of all elements surrounding A[i,j] in the matrix A, i.e., all elements in the immediate neighbourhood of A[i,j]. Take care while handling the elements at the boundaries.


There are no inputs or outputs. You just need to write a function with following parameters and return value-

Parameters→ A: A square matrix

Return value→ B: A square matrix containing the sums

#### Skeleton code for function:

```
def f(A):
    #your code goes here
    return B
```
where A and B are the matrices.

#### Example:

If A is 

1  2  3

4  5  6

7  8  9

then B should be

11 19 13

22 40 27

17 31 19

#### Grading System:

10 points for correct output.

30 points for submitting the program with the least number of characters. (You will be given points relatively out of 30 depending on the least number of characters used and the number of characters used by you.)

PS: We will be counting newline and white spaces as well.

#### Coding rules:
Please only use python to code your answers.

Send your entries as `.txt` files (notepad files) and name them `Name_Roll Number.txt`

#### Deadline: 
7th May, 7:00 PM

#### Winning Entries:

Here are the winning codes !!

#### MS21 : Jasteg Singh MS21042

##### 704 characters

```
def codegolf(A=list):
  for n in range(0,len(A)): 
    if n**2==len(A):
    B=[]
    for i in range(0,len(A)):
      if (i+1)<len(A) and (i+n)<len(A) and (i+n+1)<len(A) and (i+n-1)<len(A) and (i-1)<len(A) and (i-n)<len(A) and (i-n+1)<len(A):
       if (i+n-1)<len(A) and (i+1)>0 and (i+n)>0 and (i+n+1)>0 and (i+n-1)>0 and (i-1)›0 and (i-n)›0 and (i-n+1)>0 and (i+n-1)›0: 
        B.append(A[i+1]+A[i+n]+A[i+n+1]+A[i+n-1]+A[i-n]+A[i-n-1]+A[i-n+1]+A[i-1])
    for x in range(0,len(B)): 
      for y in range(1,n):
        if x==y*(n-1)+y-1 or x==y*(n-1)+y-2:
         B[x]='n'
    j=0
    for h in range(0,len(B)):
     if B[h]=='n':
      j=j+1
    for s in range(0,j): 
      B.remove('n')
    return(B)
```


#### MS19, MS18, MS17, Int PhD, PhD: Baruva TS MS19056

#### 170 characters

```
def f(m):
  n=len(m)
  return [[sum([sum(x) for x in [x[max(0,j-1):min(len(x),j+1)+1] for x in m[max(0,i-1):min(n,i+1)+1]]])-m[i][j] for j in range(n)] for i in range(n)]
```

###### Note: Grading was based on code size; spaces and newlines were considered




