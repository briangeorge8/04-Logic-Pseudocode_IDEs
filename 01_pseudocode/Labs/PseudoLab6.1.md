## 1. What is an off-by-one error?

A request to reference a position that does not exist

## 2.  Look at the following pseudocode:
```
Constant Integer SIZE = 10
Declare Integer values[SIZE]
```
How many elements does the array have?
10

What is the subscript of the first element in the array?
values[0]

What is the subscript of the last element in the array?
values[9]

## 3. Look at the following pseudocode:
```
Constant Integer SIZE = 3
Declare Integer numbers[SIZE] = 1, 2, 3
What value is stored in numbers[2]?
3

What value is stored in numbers[0]?
1
```

## 4. A program uses two parallel arrays named customerNumbers and balances. The customerNumbers array holds customer numbers and the balances array holds customer account balances. If a particular customer’s customer number is stored in customerNumbers[187], where would that customer’s account balance be stored?

## 5. Look at the following pseudocode array declaration:
```
Declare Real sales[8][10]
```
How many rows does the array have?
8

How many columns does the array have?
10

How many elements does the array have?
80

Write a pseudocode statement that stores a number in the last column of the last row in the array.
arrStuff[arrStuff.rows.count - 1][arrStuff.columns.count - 1] = 5

##  6. Write a pseudocode declaration for a String array initialized with the following strings: "Einstein", "Newton", "Copernicus", and "Kepler".
string[] arrAlphanumerics = { "Einstein", "Newton", "Copernicus", "Kepler" }
or
Declare String arrAlphanumerics[4] = "Einstein", "Newton", "Copernicus", "Kepler"


## 7. Assume names is an Integer array with 20 elements. Design a For loop that displays each element of the array.
For(i = 0; i < 20; i++)
    Display arrInt[i].tostring()

## 8. Assume the arrays numberArray1 and numberArray2 each have 100 elements. Design an algorithm that copies the values in numberArray1 to numberArray2.
for(i = 0; i < 100; i++)
    numberArray2[i] = numberArray1[i]

## 9. Assume the following declarations appear in a pseudocode program:
```
Constant Integer SIZE = 100
Declare Integer firstArray[SIZE]
Declare Integer secondArray[SIZE]
```
Also, assume that values have been stored in each element of firstArray. Design an algorithm that copies the contents of firstArray to secondArray.

for(i = 0; i < 100; i++)
    numberArray2[i] = numberArray1[i]


## 10. Design an algorithm for a function that accepts an Integer array as an argument and returns the total of the values in the array.

Function Integer GetTotal(Integer[] arrNumbers)
    Integer intTotal = 0
    foreach (Integer intNum in arrNumbers)
        intTotal += intNum
    Return intTotal

## 11. Write a pseudocode algorithm that uses the For Each loop to display all of the values in the following array:
```
Constant Integer SIZE = 10
Declare Integer values[SIZE] = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
```

Foreach (Integer intNum in values)
    Display intNum

