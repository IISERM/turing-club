## Week 6

A race car is faster on newer tires compared to older ones. Imagine you are x seconds behind the lead car after lap 1. You both have the same tyres and they are of the same age. With each lap, your tyres degrade and you become slower compared to your first lap. This loss in time is given by the equation, 1.2^(0.38*a) - 1 where a is the tyre age (in laps).  The same situation applies to the car in front.

Your goal as the lead race simulator is to find the best lap at which to pit and change your car’s tyres such that you defeat the car in front. As you also want to show off to your opponents because you are definitely not a layman, you want the time difference at the end of the race to be as small as possible. 

Also, remember pitting and changing your tyres also takes time which you will have to cover up by racing as fast as you can.

#### Input:

- Number of laps in the race

- Time difference between you and the car in front 

- Time taken while you pit (default value = 21 sec)

#### Output:

- If it is possible to beat the car, output the lap at which you should pit.

- If it is impossible to beat the car at whatever lap you could pit, output the word 'IMPOSSIBLE'.

#### Example:

#### Input: 

```
20
1.0 
16.0 
```          

#### Output:

```
13
```

#### Grading System:

- 10 points for getting the correct output.

- 30 pts for submitting the program with the least execution time. (You will be given points relatively out of 30 depending on the smallest time of execution and your time of execution.)

#### Coding rules:

- Please only use python to code your answers.

- Send your entries as `.txt` files and name them as `Name_Roll Number.txt`

 

#### Deadline:

18th May, 9:00 PM

You have exactly 1 week to send in your entries.

 
#### Winning Entries:

Here are the winning codes !!

#### MS20 : Harsh Raj MS20161

```
n=int(input())
c=float(input())+float(input()or 21)
f=1.07174**n
e=(c*0.07174-f-1)/2
d=e**2-f
if d>0:
    y=d**0.5-e
    if y>0:
        z=int((y**(1/100000)-1)/6.92835e-07)
        print(z)
    else:print('IMPOSSIBLE')
else:print('IMPOSSIBLE')
```

#### MS19, MS18, MS17, Int PhD, PhD: Baruva TS MS19056

```
def func(num_laps,time_diff,pit_time=21):
  a = []
  for i in range(1,num_laps+1,1):
    a.append(1.2**(0.38*i)-1)
  list1=[]
  list2=[]
  for i in range(0,num_laps,1):
    t = time_diff-sum(list(a[:i]+a[0:num_laps-i]))+pit_time
    if t<0:
      list1.append(abs(t))
      list2.append(i)
  if len(list1)>0:
    min_val = min(list1)
    ind = list1.index(min_val)
    result = list2[ind]
  if len(list1)==0:
    result = "IMPOSSIBLE"
  if num_laps>23:
    result="IMPOSSIBLE"
  return(result)
```