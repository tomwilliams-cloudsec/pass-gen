# pass-gen
Using the import Random Function in VScode to create unique passwords 
Password Generator using Random Function Explained 

	1	Code 

import random
Explanation
The program begins by importing Python's built-in random module. The module which contains functions for generating random characters and making random selections.
We will be specifically using the .sample() function from the random module later in our program to randomly pick characters to make up our final password.

2. Code
capital_let = "QWERTYUIOPASDFGHJKLZXCVBNM"
small_let = "qwertyuiopasdfghjklzxcvbnm"
numbers = "1234567890"
special_char = "?,.<>!%$]{£*)|#@"
Explanation
we have created several strings stored inside 4 variables, containing all possible characters we can use for our password generator. In other words, the above variables are going to make up our passwords and contain all possible characters we can use for our final password. 

3. Code
upper,lower,digits,odd = True,True,True,True
Explanation
we have created 4 booleans (remember they can only be true or false), stored inside 4 variables for selecting which things we want to include in the password we are generating. These booleans will be linked to the above 4 variables (capital_let, small_let etc) later on in the code. Upper is linked with the first True boolean, Lower is linked with the second True boolean etc.

For further explanation, These four boolean variables (upper, lower, digits, odd) act as baselines to determine whether each character types will be included in the password generation.

All are set to True, meaning all character types will be used

upper: When True, uppercase letters (capital_let variable) are included in the finalpass string (the finalpass string will be explained below). This goes for the rest of the booleans.

lower: When True, lowercase letters (small_let variable) are included in the finalpass string.

digits: When True, number digits (number variable) are included in the finalpass string.

odd: When True, special characters (special_char variable) are included in the finalpass string.

4. Code
finalpass = ""
Explanation
Here we have created a string which will be our final password. This will be linked to the .sample() function later in our program. finalpass (our final password) is an empty string that will be filled with the selected character sets based on whether the above booleans have been set to True or False.

5. Code
if upper:
finalpass += capital_let
if lower:
finalpass += small_let
if digits:
finalpass += numbers
if odd:
finalpass += special_char

Explanation
This part of the code checks each boolean. So if the above variable upper is set to True, capital_let will be appended to finalpass.
The += operator lets us merge the values of finalpass and capital_let together and assign the resultant value to a variable.
if all the above variables (lower, digits etc) are set to true, then they are going to be included in the final string which we have called finalpass.
After what has been set, finalpass will contain a concatenated string of all the characters that can be used in the passwords.

6. Code
length = 20
howmuch = 10
Explanation
Here we have set the length of the password. We have also set how many passwords we want our program to generate.
length: Specifies that each password will be 20 characters long.
howmuch: Specifies 10 passwords to be generated.


7. Code
for x in range(howmuch):
password = "".join(random.sample(finalpass,length))
print(password)
Explanation
The for loop runs/loops the howmuch variable 10 times as we have set it to 10. This creates one password per loop. Once the 10th password has been created, the loops ends and no more passwords will be created.
Then we have a variable called password that contains code. Let's go through it.
random.sample(finalpass, length) - The .sample() function is specifically a function that returns a particular length list of items, randomly selected or chosen from a given population or sequence such as list, string etc.
In our case the .sample( ) function will randomly select 20 characters from the finalpass variable. Remember finalpass contains all the strings from capital_let, small_let etc, because we set the booleans inside upper, lower etc to true!

Why will it select only 20 characters? Because we set the length to 20 previously in our code!

"".join is going to join the random 20 characters selected from the finalpass variable by the random.sample() function. into a single string to form the passwords. It will do this 10 times because of the for loop.
The 10 sets of newly formed passwords will be contained inside the password variable, which as you can see is inside the for loop!
We need some way to get those 10 passwords. Therefore, we use the print function to print out those 10 passwords for us!
