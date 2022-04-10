## Week 3

The reduced digit sum of 625 is calculated as follows:

6+2+5 = 13

1+3 = 4

Therefore, the reduced digit sum of 625 = 4

Given a certain number N, if the reduced digit sum of N is 1 then print “YES” otherwise print “NO”.

#### Input:

The first and only line of input will contain the number N.


#### Output:

“YES” If the reduced digit sum of N = 1

Otherwise,

“NO”

#### Example:

#### Input: 

```
8686

```          

#### Output:

```
YES
```

#### Grading System:

10 points for getting the correct output.

30 points for submitting the program with the least number of characters. (You will be given points relatively out of 30 depending on the least number of characters used and the number of characters used by you.)

#### Coding rules:

- Please only use python to code your answers.

- Send your entries as `.txt` files and name them as `Name_Roll Number.txt`

 

#### Deadline:

6th April, 7:00 PM

You have exactly 1 week to send in your entries.

 
#### Winning Entries:

Here are the winning codes !!

#### MS21 : Sparsha Ray MS21256

##### 37 characters

```
print('YNEOS'[int(input())%9!=1::2])
```

#### MS20 : Harsh Raj MS20161, Sachin G Iyer MS20056 

##### 38 characters

```
print(["NO","YES"][int(input())%9==1])
```

MS19, MS18, MS17, Int PhD, PhD: Kaustav Sen MS19091

#### 47 characters

```
print('NYOE S'[int(input())%9==1::2])
```

###### Note: Grading was based on code size; spaces and newlines were considered
