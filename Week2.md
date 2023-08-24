
# Logical Operators (and or) 
a = True
b = True
print(a and b)

# Comparison 

a = 2
b = 8
print(a == b)
print(b > a)
print(a != b)


# But be careful, you cannot compare non-comparable types

word = 5
print("word" < word)


# Control Flow Statements
# if elif else statements

weather = 100

if weather > 90:
    print("Nice Weather")
elif weather > 70:
    print("You need to wear winter cloths")
else:
    print("My advice Stay at Home")

# Very specific to Python, please be careful when using the next, it could lead to unexpected errors

x = 5

if x:
    print("Bingo")

# In-class Assignment

Write a Python program that uses an if-else statement to check if a number entered by the user is positive or negative. If the number is positive, print "Positive" and if it is negative, print "Negative".


print("Week2")

# statement = False
# print(statement)
# print(int(statement))

# print(type(statement))
# print(type(5))
# print(type("hello"))

# condition = True or False

# age = 20

# isAdult = age > 18

# print(isAdult)
# print(type(isAdult))

# savedPassword = 777

# userInput = (input("Please type your password:"))

# print(savedPassword == int(userInput))

weather = 100

if weather > 100:
    print("Stay at home")
else:
    print("Go outside")


# Ask user's name and GPA
# print if he is a good student or no

name = input("Type your name")
gpa = input("Provide your gpa")


try:
    isGood = int(gpa) > 2.0
    
    if isGood:
        print("{} You are the best".format(name))
    else:
        print("{} You need to study more".format(name))
except:
    print("You are not friendly user")

# Week 2 Continue

Loop Intro

# The while statement

x = 10
while x > 0:
    print(x)
    x -= 1

What makes Python Powerful

# Random number generator
import random

# Generate a random number between 1 and 100
number = random.randint(1, 100)

# Time library
import time
time.sleep(1)

Practice
"Guess the Number" game: Use a while loop to repeatedly prompt the user to guess a randomly generated number between 1 and 100. If the user's guess is incorrect, give them a hint (too high or too low) and continue the loop. If they guess correctly, print a message congratulating them and end the loop.

"Factorial Calculator": Use a while loop to calculate the factorial of a number entered by the user. The loop should continue as long as the current number being multiplied is greater than 1.

"Fibonacci Sequence Generator": Use a while loop to generate the Fibonacci sequence up to a certain number of iterations entered by the user. Print each number in the sequence as it is generated.

"Countdown Timer": Use a while loop to create a countdown timer that counts down from a user-specified number of seconds. Print the current remaining time at the end of each iteration of the loop.

"Staircase-Triangle generator"
Use a while loop to print a triangle of stars, where the number of stars in each row is incremented by one each iteration. The loop should continue until the number of stars in a row reaches a user-specified maximum number.


*
**
***
****

import random

secretnumber = random.randint(1,100)
counter = 0
while counter < 10:
    userGuess = int(input("Provide your guess"))
    counter = counter + 1

    if userGuess == secretnumber:
        print("Congratualtions!")
        break

    if userGuess > secretnumber:
        print("Higher")
    else:
        print("Lower")