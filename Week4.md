#print("Week4")

 Before we start
 
# Password checker

Ask a user to create a passowrd
Check it if it's valid

If good Ask to retype it
print on screen
Else Ask again, till provides valid

#Valid password: contains digits, uppercase and special symbols !#

# Week4 Collections: List

#1) list.append(element):

fruits = ['apple', 'banana', 'cherry']
fruits.append('orange')
print(fruits)

#2) list.extend(iterable):

fruits = ['apple', 'banana', 'cherry']
more_fruits = ['orange', 'grapes', 'mango']
fruits.extend(more_fruits)
print(fruits)

#3) list.insert(index, element):

fruits = ['apple', 'banana', 'cherry']
fruits.insert(1, 'orange')
print(fruits)

#4) list.remove(element):

fruits = ['apple', 'banana', 'cherry', 'orange']
fruits.remove('banana')
print(fruits)

#5) list.pop(index):

fruits = ['apple', 'banana', 'cherry', 'orange']
fruits.pop(1)
print(fruits)

#6) list.index(element):

fruits = ['apple', 'banana', 'cherry', 'orange']
print(fruits.index('cherry'))

#7) list.count(element):

fruits = ['apple', 'banana', 'cherry', 'banana']
print(fruits.count('banana'))

#8) list.sort():

numbers = [3, 1, 4, 2]
numbers.sort()
print(numbers)

#9) list.reverse():

numbers = [1, 2, 3, 4]
numbers.reverse()
print(numbers)

#10) list.copy():

fruits = ['apple', 'banana', 'cherry']
more_fruits = fruits.copy()
more_fruits.append('orange')

Before, let's use while + list together.
This is where power comes

Practice: 
Create a list of numbers from 1 to 10, then write a function that takes the list as an input and returns a new list with the numbers squared.

Write a program that takes a list of strings and returns a new list with all strings converted to uppercase.

Code Section From Class:

print("Week:4 Collections: List")
nums = [1,3,4,5,100]

# # append 
# nums.append(-777)
# print(nums)

# nums.insert(1,1000)
# print(nums)

# nums.extend([9,9,8,7])
# print(nums)
# # nums += [7,8,9]

# # How to delete element
# nums.pop(1) # by index
# print(nums)

# nums.remove(-777) # by value
# print(nums)

# print(nums[3]) # by index
# nums.append(5)

# print(nums.index(5))

# Warm up problem
# you have nums = [1,4,5,4]

# Print every location of value 4 print index

# word = "Hello"
# idx = 0
# while idx < len(word):
#     if word[idx] == 'l':
#         print(word[idx],idx)
#     idx += 1



# word = [1,4,5,4]
# idx = 0
# while idx < len(word):
#     if word[idx] == 4:
#         print(word[idx],idx)
#     idx += 1

# Warm up 2

# ask user to provide a number 5 times, and save user response inside of list
# print list on screen

nums = []

attempt = 0

while (attempt < 5):
    userInput = input("Type a number:")

    sign = 1

    if userInput[0] == '-':
        userInput = userInput[1:]
        sign = -1

    if userInput.isdigit():
        num = int(userInput)
        nums.append(num*sign)
        attempt += 1
    else:
        print("Try again")
    

print(nums)






# print(nums)

# print(nums[0:3]) #start inclusive,end exlusive

# print(nums[4])

# nums[0] = 1111

# print(nums)

# #copy_nums = copy.deepcopy(nums)
# copy_nums = nums[:]

# copy_nums[0] = 10000000
# copy_nums.append(-88)

# print(nums)


