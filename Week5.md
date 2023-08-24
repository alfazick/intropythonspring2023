
Week5: "Functions"

Warmp up
Today Challenge

#1
Greet user
Write a program that ask user to provide his hobbies.
Save each hobby in the list
When user provide word "stop"
Stop executing and print all of his hobbies

# Defining a user defined functions
# Before we used print function


#A function is a named list of statements.

#A function definition consists of the new function's name and a block of statements. 

#In Python 
# def namefunction():
    #code block


#A function call is an invocation of a function's name, causing the function's statements to execute.


#The function's name can be any valid identifier. A block is a list of statements



#Returning a value from a function with a return

# Idea of parameters or arguments

#Code 

# def printMSG(message):
#     print(message)
#     print(message)
#     print(message)



# printMSG("Houra!")
# printMSG("Go!")


def multiply(x,y):
    #print(x * y)
    return x * y

def addTax(price):
    return (price * 1.10) # > (price * (1 + 0.10))

itemName = input("Please give me a name the item you want to buy? ")
itemPrice = input("Please type the price of the item: ")
itemQuantity = input("Please tell me how many items you want to buy?")

print("Dear Customer. Today you bought",itemName,"for ", itemPrice, "a piece")

beforetaxtotal = multiply(int(itemPrice),int(itemQuantity))


print("You owe us", addTax(beforetaxtotal))

# 2640

# item1cost = multiply(10,20)
# item2cost = multiply(5,10)
# finalcheck = item1cost + item2cost
# print("You owe us ", finalcheck, " amounts of dollar" )


Practice: 
Create a list of numbers from 1 to 10, then write a function that takes the list as an input and returns a new list with the numbers squared.

Write a program that takes a list of strings and returns a new list with all strings converted to uppercase.




print("Week5 : Function")

# Warm up

# 1) Define a function which accepts string
# and print on screen 1 time
# 2) Function: Print string 3 times

# simple function no arguments

# def message():
#     print("Hello")
#     print("Hello")
#     print("Hello")


# simple function arguments

def message(msg):
    print(msg)
    print(msg)
    print(msg)

# message("Hello")
# message("Hi")
# message("World")

# Calculator: Assignment define 4 functions
# communicate with user and execute one of them

def add(x,y): #// int , string 
    return x + y 
    
# def multiply(x,y):

# def subtract(x,y)

# def divide(x,y):

#     if y == 0:
#         print("Wrong input")
#         return -1
#     return x / y

# def divide(x,y):

#     while (y == 0):
#         y = int(input("Type the correct denominator: "))
#     return x / y

    
# num1 = int(input("Type a number: "))
# num2 = int(input("Type a number: "))

# operation = input("Type the operation: ")

# if operation == "+" or operation == "add" or operation == "addition":
#     result = add(num1,num2)
#     print(result)
    

# if operation == "/":
#     result = divide(num1,num2)
#     print(result)



# nums = []
# num = 1
# while num < 11:
#     nums.append(num)
#     num +=1
# print(nums)

# print(range(1,11))
# print(list(range(1,11)))

# # List comprehensition
# nums = [num for num in range(1,11)]
# # print(nums)

# def make_square(nums):
#     ans = []
#     idx = 0
#     while idx < len(nums):
#         ans.append(nums[idx] * nums[idx])
#         idx +=1

#     return ans

        

# ans = make_square(list(range(1,11)))

# print(ans)

# def print_message(word,num):
#     for i in range(num):
#         print(word)

# def get_num():
#     userInput = ""
    

#     while not userInput.isdigit():
#         userInput = input("Type number: ")

#     num = int(userInput)
#     return num

# print_message("hi",get_num())

# def capitalize(word):
#     return word.upper()

# print(capitalize("hello"))

words = ["hello", "hi","world"]
print(words)
# def capital_printer(w):
#     for i in range(len(w)):
#         w[i] = w[i].upper()

        
def capital_printer(w):
    capital_words = []

    for word  in w:
         capital_words.append(word.upper())

    return capital_words

    
words = capital_printer(words)
print(words)
