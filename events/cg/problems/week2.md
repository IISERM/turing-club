<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

## Week 2

You are on a heist to rob the world’s largest metal reservoir. You have brought a bag along with you which can only hold M kgs at maximum. There are N types of metals in there, in the form of bricks. Each brick of i-th metal weighs $w_{i}$ kgs and holds a value of $ $v_{i}$  in the black market. Write a program to calculate the maximum value of metals which you can take with you. 

#### Input:

- First line of input contains two non positive integers N and M.
- Second line contains N space separated non negative integers $w_{1}, w_{2}, w_{3},..., w_{N}$ where $w_{i}$ represents the weight of one brick of i-th metal.
- Third line contains N space separated positive integers $v_{1}, v_{2}, v_{3}, …, v_{N}$ where $v_{i}$ represents the value of one brick of i-th metal in black market .


#### Output:

A single integer which is the maximum money which you can get from the black market.

#### Example:

#### Input: 

```
4 8                 
1 3 4 5
10 40 50 70

```          

#### Output:

```
110
```

#### Grading System:

10 points for getting the correct output.

30 pts for submitting the program with least execution time. (You will be given points relatively out of 30 depending on the smallest time of execution and your time of execution.)

#### Coding rules:

- Please only use python to code your answers.

- Send your entries as `.txt` files and name them as `Name_Roll Number.txt`

 

#### Deadline:

30th March, 6:00 PM

You have exactly 1 week to send in your entries.

 
#### Winning Entries:

Here are the winning codes !!

#### MS21 : Atul Kumar Tiwary MS21012

##### 0.243 Seconds

```
N,M=[int(x) for x in input().split()]
w=[int(x) for x in input().split()]
v=[int(x) for x in input().split()]
vpw=[v[i]/w[i] for i in range(N)]

def maxv():
  max=-1
  for i in range(len(vpw)):
    if max<vpw[i]:
      max=vpw[i]
      c=i
  for i in range(len(vpw)):
    if vpw[c]==vpw[i] and w[c]<w[i]:
      c=i
  return[max,c]

sum=0
while M>0:
  mv=maxv()[0]
  i=maxv()[1]
  if w[i]<=M:
    t=M//w[i]
    sum=sum+(t*(v[i]))
    M=M-(t*(w[i]))
  else:
    vpw.remove(vpw[i])
    v.remove(v[i])
    w.remove(w[i])
  if v==[]:
    break
print(sum)
```

#### MS20 : Harsh Raj MS20161 

##### 0.287 seconds

```
x = str(input())
y = str(input())
z = str(input())

n = int(x.split()[0])
s = int(x.split()[1])
b = list(map(int,y.split()))
c = list(map(int,z.split()))

b = [i/j for i,j in zip(b,c)]
b,c = zip(*sorted(zip(b,c)))
b = list(b)
c = list(c)
d = b
b = [i*j for i,j in zip(b,c)]

v = 0
k = 0
e = 0
f = 0
nu = 1
while(s!=0) and (k!=n):
    if e < n and nu !=0:
        nu = mu = d.count(d[e])-1
        if nu > 0:
            for i in range(0,nu):
                f = e
                for j in range(0,mu):
                    if c[f+1]*(s//b[f+1]) > c[f]*(s//b[f]):
                        c[f],c[f+1] = c[f+1],c[f]
                        b[f],b[f+1] = b[f+1],b[f] 
                f+=1
                mu-=1
    v = v + c[k]*(s//b[k])
    s = s%b[k]
    k += 1
    nu += 1
    if e < n:
        e += d.count(d[e])
print(v)
```

MS19, MS18, MS17, Int PhD, PhD: Baruva TS MS19056

#### 0.291 seconds

```
st3 = input()
st = st3.split()
n = int(st[0])
cap = int(st[1])
st2 = input()
w = st2.split()
wt = [int(j) for j in w]
st1 = input()
v = st1.split()
val = [int(i) for i in v]

def unbounded_knapSack(cap, wt, val, n):

    dp = [0] * (cap + 1)
    for c in range(1, cap + 1):
        mx = 0
        for i in range(0, n):
            if wt[i] <= c:
                rembagc = c - wt[i]
                rembagv = dp[rembagc]
                tbagv   = rembagv + val[i]
                if (tbagv > mx):
                    mx = tbagv
                    dp[c] = mx
    return dp[cap]

print(unbounded_knapSack(cap, wt, val, n))
```

###### Note: Grading was purely based on the time taken for execution
