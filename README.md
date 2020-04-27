# Project-Euler-4
My C++ solution to problem 4 on project euler at https://projecteuler.net/archives

The problem is stated as follows:

*A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99.*

*Find the largest palindrome made from the product of two 3-digit numbers.*


My solution is a brute force method that uses a nested for loop to test all
possible combinations of two three-digit numbers. In each iteration of the
nested for loop, the product is calculated and then passed as an argument to
a function called isPal(). The function tests whether the product is a 
palindrome by calling on another function, reverseNum, which returns the reverse
number of whatever number is passed to it. 

It does this by taking advantage of the
fact that any number divided by 10 has a remainder of said number's last digit.
The remainder is calculated using the % operator. The remainder/last digit is then
appended to an int called revNum. The number is finally divided by 10 in order to
remove the last digit. All of this is done within a while loop that ends when the 
number reaches 0, so that the entire number is reversed via the above method of 
appending to revNum and chopping the last digit of the original.

If the number is a palindrome (isPal() returns true), a set of if and else if 
statements assigns it to the variable greatestPal if it is the greatest palindrome 
found yet. When the nested for loops complete, greatestPal is then outputted to a console.
