# Reversing-a-Number-using-Recursion-in-CPP

Reversing a Number using Recursion in C++
 

Here, in this page we will discuss the program for reversing a number using recursion in C++ programming language. We are given with a number and need to print the reverse of the given number. We will discuss the both recursive and non-recursive method to find the reverse of the given input number.

Example :

Input : 1234
Output : 4321
Reversing a number using recursion in C++
Method 1 (Using Recursion) :
Create a reverse(int n), a recursive function of void type.
Base condition will be : if (n <10)  , then print(n) and return.
Otherwise, print(n%10) and call function reverse(n/10).
 
Time and Space Complexity
Time Complexity : O(d) where, d denotes the number of digits in number n.
Space Complexity : O(1)
Reversing the number
Code for Reversing a Number Using Recursion in C++
Run
#include <bits/stdc++.h>
using namespace std;

void reverse(int n)
{

   // base condition to end recursive calls
   if (n < 10) {
      cout<<n;
      return;
   }

   else{
      cout<<n%10;
      reverse(n/10);
   }
}

// Driver Program
int main()
{
   int n=1234;
   reverse(n); //Calling recursive function
   return 0;
}
Output :

4321
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Prime Number

Largest element in an array

Method 2 (Using  Loop) :
Create a variable to store the reversed number, say it is rev and initialized it with 0.
Run a loop till n is greater than 0.
Inside the loop, create a variable say rem to hold the unit digit of number n.
Set, rem = n%10.
and rev = rev*10 + rem.
Then decrement n as n = n/10.
After termination of loop print(rev)
Time and Space Complexity
Time Complexity : O(d) where, d denotes the number of digits in number n.
Space Complexity : O(1)
Code for Reversing a Number Using loop in C++
Run
#include <bits/stdc++.h>
using namespace std;

void reverse(int n)
{

   int rev=0;
   while(n>0){

     int rem=n%10;
     rev = rev*10 + rem;
     n /= 10;
   }

   cout<<rev;
}


// Driver Program
int main()
{
   int n=1234;
   reverse(n); 
   return 0;
}
Output :

4321
