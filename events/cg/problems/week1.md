## Week 1

Print all the natural numbers from 1 to N (1 and N inclusive). Print “CODE” if it is a multiple of 3, print “GOLF” if it is a multiple of 7, and print “CODEGOLF” if it is a multiple of 3 and 7 both. Write a solution that uses the minimum number of characters. 

#### Input:

There must be only one line of input and it contains a positive integer N which is the upper limit to which the numbers are to be printed.

#### Output:

Print N separate lines containing the numbers from 1 to N.

For each multiple of 3, print "CODE" instead of the number. 

For each multiple of 7, print "GOLF" instead of the number.

For numbers that are multiples of both 3 and 7, print "CODEGOLF" instead of the number.

#### Example:

#### Input: 

`10`          

#### Output:

```
1
2
CODE
4
5
CODE
GOLF
8
CODE
10
```

#### Grading System:

10 points for getting the correct output.

30 points for using the least number of characters amongst all the submitted solutions. (You will be graded relatively for the number of characters used. Lesser the number of characters used, more the extra points you'll get.)

#### Coding rules:

Please only use python to code your answers.

Code your answers in a colab notebook and send us the link to it (we know it’s slow, but it makes your job of uploading and our job of checking, easier)

 

#### Deadline:

You have exactly one week to send your responses in. Deadline: 23rd March, 2022, 12:00PM


#### Winning Entries:

Here are the winning codes !!

#### MS21 : Armandeep Singh MS21021 

##### 69 Characters

```
for x in range(int(input())):print(x%3//2*'CODE'+x%7//6*'GOLF'or x+1) 
```

#### MS20 : Aswin R Nair MS20028

##### 102 Characters

```
i=int(input())
for x in range(1,i+1):
   o=[x,"CODE","GOLF","CODEGOLF"]
   print(o[1*(x%3==0)+2*(x%7==0)])
```

#### MS19, MS18, MS17, Int PhD, PhD : Akshay Shankar MS18117 & Dhruva Sambrani MS18163

##### 71 Characters

```
for i in range(int(input())):print('CODE'*(i%3>1)+'GOLF'*(i%7>5)or i+1) 
```

###### Note: We haven't considered newlines and spaces for this problem 
