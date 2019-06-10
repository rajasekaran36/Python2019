# Histogram Analysis
## Step 0 : *List contains some numbers*

 - Create a numbers list that contains some unique numbers
 - Display the list

**Code**
 ```python
 numbers = [2,4,5,1,6,7,8,3]
print(numbers)
```
**Output**
```shell
[2, 4, 5, 1, 6, 7, 8, 3]
```


## Step 1 : *List contains some duplicate numbers*

 - Create a numbers list that contains some numbers and that constains duplicates
 - Display the list

**Code**
 ```python
 numbers = [2,4,5,1,6,7,8,3,1,4,7,3]
print(numbers)
```
**Output**
```shell
[2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
```

## Step 2 : *Finding the each numbers count and display*

 - Create a numbers list that contains some numbers and that constains duplicates
 - Display the list
 - Display the counts of each number


**Code**
 ```python
from collections import defaultdict
numbers = [2,4,5,1,6,7,8,3,1,4,7,3]
print("List contain :", numbers)
histo = defaultdict(int)
for key in numbers:
    histo[key] += 1

print("Count of each number in the list")
print("--------------------------------")
for key in histo:
    print(key, "--",histo[key])
```
**Output**
```shell
List contain : [2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
Count of each number in the list
--------------------------------
2 -- 1
4 -- 2
5 -- 1
1 -- 2
6 -- 1
7 -- 2
8 -- 1
3 -- 2
```
## Step 3 : *Finding the each numbers count and display like a graph (Histogram)*

 - Create a numbers list that contains some numbers and that constains duplicates
 - Display the list
 - Display the counts of each number
 - Display number and @ symbol for each occurance

**Code**
 ```python
from collections import defaultdict
numbers = [2,4,5,1,6,7,8,3,1,4,7,3]
print("List contain :", numbers)
histo = defaultdict(int)
for key in numbers:
    histo[key] += 1

print("Histogram of the list")
print("---------------------")
for key in histo:
   print(key, "@"*histo[key])
```
**Output**
```shell
List contain : [2, 4, 5, 1, 6, 7, 8, 3, 1, 4, 7, 3]
Histogram of the list
---------------------
2 @
4 @@
5 @
1 @@
6 @
7 @@
8 @
3 @@
```
## Step 4 : *Lets try with some random numbers using random class (Histogram)*

 - Create a numbers list that contains random values that has lower and upper bounds for count and values.
 - Display the list
 - Display the counts of each number
 - Display number and @ symbol for each occurance

**Code**
 ```python
from collections import defaultdict
import random

#Values used for random functions
mincount = 20
maxcount = 200
minvalue = -10
maxvalue = 15

#Source list
numbers = []

#Random size is computed
size_of_list = random.randint(mincount,maxcount)

#List of random number is generated

for i in range(size_of_list):
    numbers.append(random.randrange(minvalue,maxvalue+1))
print("List contain :", numbers)
histo = defaultdict(int)
for key in numbers:
    histo[key] += 1

print("Histogram of the list")
print("---------------------")
for key in histo:
    print(f"{key:2}", "@"*histo[key])
```
**Output**
```shell
List contain : [6, -10, -7, -7, -4, 2, 11, 3, -3, 12, 0, -6, 14, -7, 13, -8, -5, -5, 12, -4, 1, 15, 9, 7, 11, 15, 1, 2, 6, 9, -8, 10, 2, -8, 15, -2, -6, 7, 0, 4, 10, 2, -3, 1, 4, -9, 4, 14, -7, -4, 3, -2, -7, 3, -9, 10, 10, 5, -9, 7, -9, -6, 13, -1, 8, -10, 13, 9, 4, 5, 3, -2, -2, 11, -3, -3, -2, -7, 8, 7, 13, 13, -8, 2, 0, 1, 6, -5, 1, 13, 14, 4, -3, 15, 15, 14, -3, -5, -2, 7, 4, 9, -5, -6, 13, 10, -3, 5, -5, 14, 13, 14, -9, 9, -7, 15, 6, 13, 2, 14, 4, 8, 7, -3, 15, 13, 6, 3, -5, -8, 10, -7, -3, 13, 5, 3, 13, -4, -6, 0, -2, -9, 12, 5, 10, 8, -1, 10, 3, 1, -3, 4, 1, 2, 15, 6, 6, 0, 4, 11, -8, -2, 7, 10, -3, -1, 6, 1, 0, -6, 10, 8, 6, 2, -4, -1, -4, 12, -1, 6, 13, 11, 6, -7, 4, 13, 1, -6, -2, -2, -10, 10, 6, -3, 14]
Histogram of the list
---------------------
 6 @@@@@@@@@@@@
-10 @@@
-7 @@@@@@@@@
-4 @@@@@@
 2 @@@@@@@@
11 @@@@@
 3 @@@@@@@
-3 @@@@@@@@@@@@
12 @@@@
 0 @@@@@@
-6 @@@@@@@
14 @@@@@@@@
13 @@@@@@@@@@@@@@
-8 @@@@@@
-5 @@@@@@@
 1 @@@@@@@@@
15 @@@@@@@@
 9 @@@@@
 7 @@@@@@@
10 @@@@@@@@@@@
-2 @@@@@@@@@@
 4 @@@@@@@@@@
-9 @@@@@@
 5 @@@@@
-1 @@@@@
 8 @@@@@
```
## Step 5: *Lets try with some random numbers using random class (Histogram) but ordered (based on key)*

 - Create a numbers list that contains random values that has lower and upper bounds for count and values.
 - Display the list
 - Display the counts of each number
 - Sort tupple based on the key
 - Display number and @ symbol for each occurance

**Code**
 ```python
from collections import defaultdict
import random

#Values used for random functions
mincount = 20
maxcount = 200
minvalue = -10
maxvalue = 15

#Source list
numbers = []

#Random size is computed
size_of_list = random.randint(mincount,maxcount)

#List of random number is generated

for i in range(size_of_list):
    numbers.append(random.randrange(minvalue,maxvalue+1))
print("List contain :", numbers)
histo = defaultdict(int)
for key in numbers:
    histo[key] += 1

histo_order = sorted(histo.items())
print("Ordered Histogram of the list")
print("---------------------")
for (key,value) in histo_order:
    print(f"{key:2}", "@"*value)
```
**Output**
```shell
List contain : [7, 14, -2, -8, 0, 5, 8, 3, 12, 9, 15, 0, 6, 14, 12, -6, -7, 13, 14, -2, 1, 13, -8, 11, -4, 4, -8, 6, -10, 11, -5, -7, 7, 8, -2, 1, -9, -7, 11, 14, 3, 7, -3, 10, 8, 13, 10, 3, -3, -5, 12, -6, 15, 15, 8, 5, 15, 13, -2, 2, 7, -3, -7, -4, 10, 11, 3, -1, 4, -1, 5, 15, 13, 15, -1, 15, 15, 13, -3, -10, 2, -4, -7, 4, -2, 0, 15, 7, -8, -6, 15, -9, -2, 13, 0, 9, -8, 10, 7, -9, 8, -5, 10, 14, 2, 2, 9, 7, 14, -5, -4, 11, -4, -2, 4, 2, 9, -7, 14, 14, -8, 12, 2, 12, 14, -2, 9, -10, 10, 15, 3, 11, 9, 15, -8, 3, -1, -9, 9, -6]
Ordered Histogram of the list
---------------------
-10 @@@
-9 @@@@
-8 @@@@@@@
-7 @@@@@@
-6 @@@@
-5 @@@@
-4 @@@@@
-3 @@@@
-2 @@@@@@@@
-1 @@@@
 0 @@@@
 1 @@
 2 @@@@@@
 3 @@@@@@
 4 @@@@
 5 @@@
 6 @@
 7 @@@@@@@
 8 @@@@@
 9 @@@@@@@
10 @@@@@@
11 @@@@@@
12 @@@@@
13 @@@@@@@
14 @@@@@@@@@
15 @@@@@@@@@@@@
```
## Step 6: *Lets try with some random numbers using random class (Histogram) but ordered (based on value)*

 - Create a numbers list that contains random values that has lower and upper bounds for count and values.
 - Display the list
 - Display the counts of each number
 - Reverse key and values
 - Sort tupple based on the value
 - Display number and @ symbol for each occurance

**Code**
 ```python
from collections import defaultdict
import random

#Values used for random functions
mincount = 20
maxcount = 200
minvalue = -10
maxvalue = 15

#Source list
numbers = []

#Random size is computed
size_of_list = random.randint(mincount,maxcount)

#List of random number is generated

for i in range(size_of_list):
    numbers.append(random.randrange(minvalue,maxvalue+1))
print("List contain :", numbers)
histo = defaultdict(int)
for key in numbers:
    histo[key] += 1

histo_order = sorted(histo.items())
print("Ordered Histogram of the list")
print("---------------------")
for (key,value) in histo_order:
    print(f"{key:2}", "@"*value)
```
**Output**
```shell
List contain : [-10, 12, 8, -3, 6, 8, -3, 13, -10, -10, 15, -4, -7, 11, -8, 3, 1, 4, 7, 2, 2, -7, 2, -6, 12, 4, 1, 4, 14, 2, 14, 7, 4, -9, 5, 8, 15, 15, 5, -9, -3, -10, 3, 9, -10, 7, 2, -10, -5, 4, -10, 14, 2, -5, 8, 10, 4, 15, 10, 5, 10, 3, 0, -6, 13, -9, 10, 10, -8, -1, 4, -7, 6, -1, 4, -8, 0, 15, 13, 15, -5, 2, -5, 6, -1, -5, -3, 8, -6, -2, 2, -9, 15, 4, 3, 0, -8, 15, -5, -8, 12, -1, -2, -4, 7, -5, -9, -2, -9, 15, 4, -7, -9, -7, -9, 6, 1, 8, 6, 5, 11, 13, -9, 8, 15, 1, -7, 3, -8, -7, 7, -1, -6, 6, 4, -4, 2, 15, -3, -10, 10, 8, 5, 2, 9, -4, 0, -8, -2, 3, -8, -7, 5, 10, -5, -4, 8, -9, 5, 6, 6, 12, 4, 11, 5, 6, -6, 12, 6, -3, 9, 1, 12, -7, -4, 5, -8, 6, -5, -7, -9, 11, 4, -8, 13, -1, 12, -7, 0, 15, -10, 10]
Ordered Histogram of the list
-----------------------------
 4 @@@@@@@@@@@@@
15 @@@@@@@@@@@@
 6 @@@@@@@@@@@
-7 @@@@@@@@@@@
-9 @@@@@@@@@@@
 2 @@@@@@@@@@
-8 @@@@@@@@@@
 8 @@@@@@@@@
 5 @@@@@@@@@
-5 @@@@@@@@@
-10 @@@@@@@@@
10 @@@@@@@@
12 @@@@@@@
 3 @@@@@@
-1 @@@@@@
-3 @@@@@@
-4 @@@@@@
13 @@@@@
 7 @@@@@
 1 @@@@@
 0 @@@@@
-6 @@@@@
11 @@@@
-2 @@@@
14 @@@
 9 @@@
```
# Cyber dojo
[Final Solution](https://cyber-dojo.org/review/show/QLPTrk?was_index=33&now_index=34&filename=undefined)

# Function Based 
## Program 1
**Code**
```python
################################
# Program No 1
# using dictionary to build the histogram
#   - using a randomizer for input
#   - functionally decomposing the logic 
#
#################################
# Build a histogram

import random
# build a random list 
# returns a list containing numbers 1 <= n <= maxval
# the list will contain n elements where
#   mincount < n < maxcount 
def random_list(mincount, maxcount, maxval, minval=1): 
  size = random.randint(mincount, maxcount)
  alist = []
  for _ in range(size):
    alist.append(random.randrange(minval, maxval+1))		
  return alist

arlist = random_list(50, 120, 20, -10)
print("A random list", arlist)


# returns a list containing tuples with 
# value and frequency, aka a histogram
from collections import defaultdict
def generate_histogram(arlist):
  counters = defaultdict(int) #inits value to 0
  for number in arlist:
	  counters[number] += 1

  histogram = sorted(counters.items())
  return histogram

histo = generate_histogram(arlist)
print("A histogram with", histo)

print("Visualizing the histogram")
for i in range(len(histo)): 
  print (f'{histo[i][0]:2}', '@'*histo[i][1])
```
**Output**
```shell
A random list [-10, 7, 20, 8, 16, 0, 9, 15, -6, 16, 14, 6, 7, -6, 20, 17, 17, -1, -10, 1, -2, 2, -9, 20, 17, -6, 12, 0, -4, 20, 8, 4, 16, 8, -3, 9, 17, 13, 0, 9, 12, 17, -4, 9, 17, 9, 3, 12, 10, -1, -8, 5, 11, -9, 12, -6, 13, 7, 6, 17, 18, 20, 13, -1, -1, -1, 9, -2, -8, 15, 6, 11, 3, -4, 9, -8, 12, -8, 5, 19, 6, 4, 4, 5, 2, 10, 5, -6, 10, 20, -3, 1, 5, 5, 20, 2, 2, -2, 5, 16, 6, -6, -4, 3, -5, 16, -5, 16, 17, 13, -7, -8, 19, -8, 1, 20, -3]
A histogram with [(-10, 2), (-9, 2), (-8, 6), (-7, 1), (-6, 6), (-5, 2), (-4, 4), (-3, 3), (-2, 3), (-1, 5), (0, 3), (1, 3), (2, 4), (3, 3), (4, 3), (5, 7), (6, 5), (7, 3), (8, 3), (9, 7), (10, 3), (11, 2), (12, 5), (13, 4), (14, 1), (15, 2), (16, 6), (17, 8), (18, 1), (19, 2), (20, 8)]
Visualizing the histogram
-10 @@
-9 @@
-8 @@@@@@
-7 @
-6 @@@@@@
-5 @@
-4 @@@@
-3 @@@
-2 @@@
-1 @@@@@
 0 @@@
 1 @@@
 2 @@@@
 3 @@@
 4 @@@
 5 @@@@@@@
 6 @@@@@
 7 @@@
 8 @@@
 9 @@@@@@@
10 @@@
11 @@
12 @@@@@
13 @@@@
14 @
15 @@
16 @@@@@@
17 @@@@@@@@
18 @
19 @@
20 @@@@@@@@
```
## Program 2
A histogram contains bins (lower bound, upper bound), and statistical values are dropped into these bins. Eventually, the histogram is visualized based on the bin counts. This type of histogram is what is used in more statistical analysis.
**Code**
```python
################################
# Program No 5
# using tuple as key in a dictionary 
# to build bins of values for 
# visualization 
#
# Refer https://datavizcatalogue.com/methods/histogram.html 
#
#################################
# Build a histogram

import random
# build a random list 
# returns a list containing numbers 1 <= n <= maxval
# the list will contain n elements where
#   mincount < n < maxcount 
def random_list(mincount, maxcount, maxval, minval=1): 
  size = random.randint(mincount, maxcount)
  alist = []
  for _ in range(size):
    alist.append(random.randrange(minval, maxval+1))		
  return alist

maxval, minval = 100, 10
arlist = random_list(40, 200, maxval, minval)
#print("A random list", arlist)

# returns a list containing tuples with 
# value and frequency, aka a histogram
from collections import defaultdict
def generate_histogram(arlist):
  counters = defaultdict(int) #inits value to 0

  bincount = 10
  binwidth = (maxval-minval)/bincount
  #minval = min(arlist)
  #maxval = max(arlist)
  points = [p for p in range(minval, maxval+1, int(binwidth))]
  
  bins = [(start, end-1) if end != maxval else (start, end) \
          for (start, end) in zip(points, points[1:])
  ]
	#bins.append(points[-1])
  
  for number in arlist:
    for start, end in bins: 
      if start <= number <= end: 
        counters[(start, end)] += 1

  return counters 

histo = generate_histogram(arlist)
print("A histogram with", histo.items())

print("Visualizing the histogram")
for bin in histo.items(): 
  print (f'{str(bin[0]):>10}', '@'*bin[1])

# Ordered histogram 
o_histogram = sorted(
	[(v, k) for k, v in histo.items()], reverse=True
)

print("Visualizing the ordered histogram")
for bin in o_histogram:
  print (f'{str(bin[1]):>10}', '@'*bin[0])
```
**Output**
```shell
A histogram with dict_items([((91, 100), 15), ((64, 72), 13), ((37, 45), 19), ((55, 63), 9), ((82, 90), 13), ((10, 18), 14), ((46, 54), 13), ((73, 81), 12), ((19, 27), 12), ((28, 36), 11)])
Visualizing the histogram
 (91, 100) @@@@@@@@@@@@@@@
  (64, 72) @@@@@@@@@@@@@
  (37, 45) @@@@@@@@@@@@@@@@@@@
  (55, 63) @@@@@@@@@
  (82, 90) @@@@@@@@@@@@@
  (10, 18) @@@@@@@@@@@@@@
  (46, 54) @@@@@@@@@@@@@
  (73, 81) @@@@@@@@@@@@
  (19, 27) @@@@@@@@@@@@
  (28, 36) @@@@@@@@@@@
Visualizing the ordered histogram
  (37, 45) @@@@@@@@@@@@@@@@@@@
 (91, 100) @@@@@@@@@@@@@@@
  (10, 18) @@@@@@@@@@@@@@
  (82, 90) @@@@@@@@@@@@@
  (64, 72) @@@@@@@@@@@@@
  (46, 54) @@@@@@@@@@@@@
  (73, 81) @@@@@@@@@@@@
  (19, 27) @@@@@@@@@@@@
  (28, 36) @@@@@@@@@@@
  (55, 63) @@@@@@@@@

```
