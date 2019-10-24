# Input Validation Exercise Workbench

Design an algorithm that prompts the user to enter a positive nonzero number and validates the input.

Function Real GetNumber()
   Real number
   Display "Enter a positive nonzero number"
   number = converttoreal(input)

   While(number < 1)
      Display "Incorrect input provided"
      Display "Enter a positive nonzero number"
      number = converttoreal(input)

   return number




Design an algorithm that prompts the user to enter a number in the range of 1 through 100 and validates the input.

Function Real GetNumber()
   Real number
   Display "Enter a number between 1 and 100 inclusive"

   number = converttoreal(input)

   while(number < 1 OR number > 100)
      Display "Incorrect input provided"
      Display "Enter a number between 1 and 100 inclusive"
      number = converttoreal(input)

   return number




Design an algorithm that prompts the user to enter “yes” or “no” and validates the input. (Use a case-insensitive comparison.)

Function string GetAnswer()
   string answer
   Display "Please enter 'yes' or 'no'"

   answer = input

   while (answer.tolower != "yes" AND answer.tolower != "no")
      Display "Incorrect input provided"
      Display "Please enter 'yes' or 'no'"
      answer = input

   return answer




Design an algorithm that prompts the user to enter a number that is greater than 99 and validates the input.

Function Real GetNumber()
   real number

   Display "Enter a number greater than 99"
   number = converttoreal(input)

   While(number < 99)
      Display "Incorrect input provided"
      Display "Enter a number greater than 99"
      number = converttoreal(input)

   return number




Design an algorithm that prompts the user to enter a secret word. The secret word should be at least 8 characters long. Validate the input.







# Debugging Exercises

Why does the following pseudocode not perform as indicated in the comments?
```
// This program asks the user to enter a value
// between 1 and 10 and validates the input.
Declare Integer value

// Get a value from the user.
Display "Enter a value between 1 and 10."
Input value

// Make sure the value is between 1 and 10.
While value < 1 AND value > 10
   Display "ERROR: The value must be between 1 and 10."
   Display "Enter a value between 1 and 10."
   Input value
End While
```

>>> The AND needs to be an OR


Why does the following pseudocode not perform as indicated in the comments?
```
// This program gets a dollar amount from the user
// and validates the input.
Declare Real amount

// Get the amount from the user.
Display "Enter a dollar amount"
Input amount

// Make sure the amount is not less than zero. If it is,
// get a new amount from the user.
While amount < 0
   Display "ERROR: The dollar amount cannot be less than 0."
   Display "Enter a dollar amount."
End While
```

>>> The user is not provided the chance to correctly enter input past the first attempt


The following pseudocode works, but it performs a case-sensitive validation of the user’s input. How could the algorithm be improved so the user does not have to pay attention to capitalization when entering a name?
```
// This program asks the user to enter a string
// and validates the input.
Declare String choice

// Get the user's response.
Display "Cast your vote for Chess Team Captain."
Display "Would you like to nominate Lisa or Tim?"
Input choice

// Validate the input.
While choice != "Lisa" AND choice != "Tim"
   Display "Please enter Lisa or Tim."
   Display "Cast your vote for Chess Team Captain."
   Display "Would you like to nominate Lisa or Tim?"
   Input response
End While
```

>>> While choice.tolower != "lisa" AND choice != "tim"