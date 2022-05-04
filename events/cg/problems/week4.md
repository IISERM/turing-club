## Week 4

Take 3 inputs from the user. Call them A, B, C respectively. The input could be 0 or 1 nothing else(You don’t need to check for this). The output(Y) printed by the program should be as per the following table-

**A**|**B**|**C**|**Y**
:-----:|:-----:|:-----:|:-----:
0|0|0|1
0|0|1|0
0|1|0|0
0|1|1|1
1|0|0|0
1|0|1|1
1|1|0|0
1|1|1|1

#### Input:

There is only a single line of input containing three space separated numbers A, B and C.


#### Output:

0 or 1 depending on the input and the table provided

#### Example:

#### Input: 

```
1 1 1

```          

#### Output:

```
1
```

#### Grading System:

10 points for getting the correct output.

30 points for submitting the program with the least number of characters. (You will be given points relatively out of 30 depending on the least number of characters used and the number of characters used by you.)

#### Coding rules:

- Please only use python to code your answers.

- Send your entries as `.txt` files and name them as `Name_Roll Number.txt`

 

#### Deadline:

17th April 2022. 5:00 PM

 
#### Winning Entries:

Here are the winning codes !!

#### MS21 : Sparsha Ray MS21256

##### 38 characters

```
a=input()
print(+(a<'0 1')^(a[4]>'0'))
```

#### MS20 : Sachin G Iyer MS20056 

##### 38 characters

```
print(bin(149)[2+int(input()[::2],2)])

```

#### MS19, MS18, MS17, Int PhD, PhD: Kaustav Sen MS19091

#### 44 characters

```
print(169>>int(input().replace(' ',''),2)&1)
```

###### Note: Grading was based on code size; spaces and newlines were considered
