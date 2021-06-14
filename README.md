# Interview_Task
# ExchangeRate Console Application
<details>
  <summary>Click to expand!</summary>

In this task you will implement an Exchange-rate integration as a console application using Python.
You can use this Exchangerate API: [https://exchangeratesapi.io/documentation/](url) to pull historical exchange rates data. 

Below are the requirements needed to implement this task:

Take a look at API documentation for implementing the integration.

For this task you may use this API_KEY: 252028bbd36fef9be2815a75083dc56c

The application will request from user some input parameters:

    1. Start_Date --> [optional] The start date of user preferred timeframe. Date format: yyyy-mm-dd
    
    2. End_Date -->   [optional] The end date of user preferred timeframe. Date format: yyyy-mm-dd
    
    3. Base -->       [optional] User will enter the three-letter currency code of his preferred base currency. 
    If it is left empty application will use EUR as default base
    
    4. Symbols -->    [optional] User will enter a list of comma-separated currency codes to limit output currencies. 
    If it is left empty then all supported currencies should be displayed
    
And will output daily historical rates between two dates of user choice

The output should be formatted as markdown table, where all entered symbols should be displayed as columns:

| base|Date|   USD   |   AUD   |   CAD   |
|-------|--------------|--------|--------|--------|
| EUR| 2012-05-01|  1.322891|  1.278047|  1.302303|
| EUR| 2012-05-02|  1.315066|  1.274202|  1. 299083|
| EUR| 2012-05-03|  1.314491|  1.280014|  1. 296868|

Since API will generate a large number of data it is important also to take into consideration the performance of the console application.

## Test Cases to be tested:
### 1.
  - Start Date: 2017-01-01
  - End Date: 2020-12-31
  - Base:     USD
  - Symbols:  ALL,EUR,CAD

### 2.
  - Start Date: 2019-01-01
  - End Date: 2021-12-31
  - Base:     USD

### 3.
(Assume end of data)
  - Start Date: 2019-01-01
  - Base:     USD

### 4.
(Assume start of data -> end of data)
  - Base:     USD

## Nice To Have: 
A new input parameter which will ask user for storing the data into csv file or not.
- StoreData into File: Y/N
</details>

# Super Stack
<details>
  <summary>Click to expand!</summary>
 
  Implement a stack that accepts the following commands and performs the operations described:

* push v: Push integer v onto the top of the stack
* pop: Pop the top element from the stack
* inc i v: Add v to each of the bottom i elements of the stack
 

After each operation, print the value at the top of the stack. If the stack is empty, print the string 'EMPTY'. 
 

**Example**

operations = ['push 4', 'push 5', 'inc 2 1', 'pop', 'pop']
  
  ![image](https://user-images.githubusercontent.com/15910141/121653198-b678a180-ca9c-11eb-9156-01beda056ba9.png)

Expected output:

4

5

6

5

EMPTY

 

**Function Description**

Complete the *superStack* in any programming language you prefer. After each operation, print the value of the stack's top element on a new line. If the stack is empty, print EMPTY instead. Taking into consideration the performance during the execution of this function is very important.

 

superStack has the following parameter(s):

    string operations[n]:  an array of strings that represent operations on the stack

 

Prints:

    string: the value of the stack's top element; if the stack is empty, print 'EMPTY', no return value is expected

 

**Constraints**

1 ≤ n ≤ 2 × 10^5 
  
-10^9 ≤ v ≤ 10^9
  
1 ≤ i ≤ |S|, where |S| is the size of the stack at the time of the operation.
  
  
It is guaranteed that pop is never called on an empty stack.
  
<details>  
  <summary>Input Format for Custom Testing</summary>

Input from stdin will be processed as follows and passed to the function.

The first line contains an integer n, the size of the array operations.

The next n lines each contain a string, operations[i].
</details>

<details>  
  <summary>Sample Case 0</summary>
  

**Sample Input**

**STDIN**   **Function**
-----       -----
12     →  operations[] size n = 12\
push 4 →  operations = ['push 4', 'pop', 'push 3', 'push 5', 'push 2', 'inc 3 1', 'pop', 'push 1', 'inc 2 2', 'push 4', 'pop', 'pop'] \
pop \
push 3 \
push 5 \
push 2 \
inc 3 1 \
pop \
push 1 \
inc 2 2 \
push 4 \
pop \
pop 
 
**Sample Output**

4 \
EMPTY \
3 \
5 \
2 \
3 \
6 \
1 \
1 \
4 \
1 \
8
 

**Explanation**

The diagram below depicts the stack after each operation:

  
![image](https://user-images.githubusercontent.com/15910141/121661353-69003280-caa4-11eb-9558-1294364a7666.png)

  
After performing each operation, print the value at the top of the stack on a new line.

 

Start with an empty stack, S, expressed as an array where the lowest indexed element is the bottom of the stack and the highest is its top. Perform n = 12 operations as given:

1. push 4: Push 4 onto the stack, so S = [4]. Print the top element, 4, on a new line. 
2. pop: Pop the top element from top of the stack, so S = []. Print 'EMPTY' on a new line. 
3. push 3: Push 3 onto the stack, S = [3]. Print 3, and the top of the stack after each of the following operations. 
4. push 5: Push 5 onto the stack, S = [3, 5]. 
5. push 2: Push 2 onto the stack, S = [3, 5, 2]. 
6. inc 3 1: Add v = 1 to the bottom i = 3 elements of the stack, S = [4, 6, 3]. 
7. pop: Pop the top element from the stack, S = [4, 6]. 
8. push 1: Push 1 onto the stack, S = [4, 6, 1]. 
9. inc 2 2: Add v = 2 to bottom i = 2 elements of the stack,  S = [6, 8, 1]. 
10. push 4: Push 4 onto the stack, S = [6, 8, 1, 4]. 
11. pop: Pop the top element from the stack, S = [6, 8, 1]. 
12. pop: Pop the top element from the stack, S = [6, 8].
</details>
  
</details>
