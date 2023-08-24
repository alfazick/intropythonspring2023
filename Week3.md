# Focus : String and String Manipulation

1) Concatenating strings:

string1 = "Hello"
string2 = "World"
concat_string = string1 + " " + string2
print(concat_string)


2) Splitting strings into substrings:

substrings = string.split(" ")
print(substrings)
Output: ['Hello', 'World']

3) Extracting substrings using indexing and slicing:

string = "Hello World"
substring = string[0:5]

4) Getting the length of a string:

string = "Hello World"
length = len(string)
print(length)

5) Converting a string to upper or lower case:

string = "Hello World"
upper_string = string.upper()
lower_string = string.lower()

6) Stripping leading or trailing whitespaces from a string:

string = "   Hello World   "
stripped_string = string.strip()


7) Replacing a substring with another string:

string = "Hello World"
new_string = string.replace("Hello", "Hi")


8) Counting the number of occurrences of a substring in a string:

string = "Hello World. Hello again World."
count = string.count("Hello")

9) Checking if a string starts with or ends with a specified prefix/suffix:

string = "Hello World"
prefix = "Hello"
suffix = "World"

if string.startswith(prefix):
    print(f"{string} starts with {prefix}")
else:
    print(f"{string} does not start with {prefix}")

if string.endswith(suffix):
    print(f"{string} ends with {suffix}")
else:
    print(f"{string} does not end with {suffix}")

10)  Checking if a string contains a specified substring:

string = "Hello World"
substring = "Wor"

if substring in string:
    print(f"{substring} is present in {string}")
else:
    print(f"{substring} is not present in {string}")

    # Code section:
    #print("Week3")
# Goal to be able to write Password checker

#Valid password: contains digits, uppercase and special symbols !#

word = "Hello"
# print(word[0])

# last_idx = len(word) - 1

# print(word[last_idx])
# print(word[-1])

# print(word.upper())
# print(word.lower())
# print(word)

# word = input("Please type a word")

# print("hello" + word.strip())

# word = "Hello {StudentName}"

# name = "John"
# print(word.replace("{StudentName}", name))
# name = "Mary"
# print(word.replace("{StudentName}", name))

# message = "Bad word"

# print(message.replace("Bad", "***"))



# string = "Hello World. Hello again World."
# count = string.count("Hello")
# print(count)


# word = "UTRGV"

# print(word[0:2])

# print(word[2:len(word)])

# print(word[2:])

# if word.startswith("UT"):
#     print("Yes",word)

# if word[:2] == "UT":
#     print("Yes",word)

# if word.endswith("RGV"):
#     print("Yes",word)

# match = "RGV"
# start = len(word) - len(match)

# if word[start:] == "RGV":
#     print("Yes",word)
    
# print(word[-3:])

# if word[-len(match):] == "RGV":
#     print("Yes",word)

# letter = "Aftyifyffof12345679"
# digit = "91523145641651563"

# # print(letter.isupper())
# # print(letter.islower())

# print(digit.isdigit())
# print(letter.isdigit())

# 1) Accept a word and capitalize it and print back
# 2) Ask user for age. make sure it's numeric
# add 10 and print back

# 3) Accept a word and print every single letter on a separate line



# while True:
#     userinput = input("Type your age?")
    
#     if userinput.isdigit():
#         res = 10 + int(userinput)
#         print("You are gonna be {} years old".format(res))
#         break
#     else:
#         print("Bad user! Type a number ")

# word[0]

word = "RGV is the Best"
idx = 0

while idx < len(word):
    print(word[idx],idx)
    idx+=1


# print(word[0])
# print(word[1])
# print(word[len(word)-1])