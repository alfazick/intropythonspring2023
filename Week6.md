print("Week 6: Sets And Dictionary")


# create a set
my_set = {1, 2, 3}

# or
my_set = set([1, 2, 3])

# print the set
print(my_set)  # Output: {1, 2, 3}

set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# union of set1 and set2
union = set1.union(set2)
print(union)  # Output: {1, 2, 3, 4, 5, 6}

# intersection of set1 and set2
intersection = set1.intersection(set2)
print(intersection)  # Output: {3, 4}

# difference of set1 and set2
difference = set1.difference(set2)
print(difference)  # Output: {1, 2}

# symmetric difference of set1 and set2
symmetric_difference = set1.symmetric_difference(set2)
print(symmetric_difference)  # Output: {1, 2, 5, 6}

#in is a Python keyword used to test whether a value or variable is present in a sequence (such as a string, list, tuple, or set).

#You can add and remove elements from a set in Python using the add(), update(), and remove() methods.
fruits = {"apple", "banana", "cherry"}
fruits.add("orange")
print(fruits)  # Output: {'banana', 'cherry', 'orange', 'apple'}

fruits = {"apple", "banana", "cherry"}
fruits.update(["orange", "kiwi"])
print(fruits)  # Output: {'banana', 'cherry', 'kiwi', 'orange', 'apple'}

fruits = {"apple", "banana", "cherry"}
fruits.remove("banana")
print(fruits)  # Output: {'cherry', 'apple'}

Problems
1) Write a function unique_characters() that takes a string as input and returns a set containing all the unique characters in the string.

2) Write a function common_elements() that takes two lists as input and returns a set containing all the elements that are common between the two lists.

3) Write a function anagrams() that takes two strings as input and returns True if the two strings are anagrams of each other (i.e., they contain the same letters, but possibly in a different order), and False otherwise.


Dictionary:

Problems

Calculate shopping card + tax


Word Frequency Counter
Write a function that takes a string as input and returns a dictionary that contains the frequency of each word in the string. The keys of the dictionary should be the words in the string, and the values should be the number of times each word appears.

Dictionary Intersection
Write a function that takes two dictionaries as input and returns a new dictionary that contains only the key-value pairs that are common to both dictionaries.


# print("Week 6: Sets")

# nums = list()
# nums = [1,2,3]
# nums.append(1)
# nums.append(1)
# nums.append(1)
# nums.append(1)
# print(nums)
# print(len(nums))


# print(len("Hello"))
# nums = set()
# nums = {1,2,3}
# nums.add(1)
# nums.add(1)
# nums.add(1)
# nums.add(1)
# print(len(nums))



# create a set guess, initially empty
# create a while loop with condition while len(guess) < 3

# ask for a number
# add to the set

# unique_nums = set()

# while len(unique_nums) < 3:
#     new_num = int(input("Provide num:"))
#     unique_nums.add(new_num)

# print(unique_nums)


# Ask a user for a word
# print how many unique characters it has

# unique_letters = set()
# word = input("Provide word:")
# for letter in word:
#     unique_letters.add(letter)

# print(len(unique_letters))

    
# for idx in range(len(word)):
#     print(word[idx])

# idx = 0
# while idx < len(word):
#     print(word[idx])
#     idx +=1

# set1 = {1, 2, 3, 4}
# set2 = {3, 4, 5, 6}

# # union of set1 and set2
# union = set1.union(set2)
# print(union)  # Output: {1, 2, 3, 4, 5, 6}

# # union
# new_union = set()

# for value in set1:
#     new_union.add(value)
# for value in set2:
#     new_union.add(value)
    
# print(new_union)

# set1.update([3,4,5,6])
# set1.update(list(set2))

# print(set1)

# ask two words
# print common letters

# some_set = {'a','b','c'}

# if 'a' in some_set:
#     print("Yes")

# if 'e' in some_set:
#     print("Yes")

# for letter in some_set:
#     print(letter)

# if "a" in "abc":
#     print("a exist")

# 1) create 2 sets
# 2) for each word add only that word letters

# 3) iterate through one set
# and check if the letter exist inside of the other
# if true it's a common letter
# print it

# word1 = input("Type the word: ")
# word2 = input("Type the word: ")

# def get_word():
#     return input("Type the word: ")

# # unique_letters1 = set(word1)
# # unique_letters2 = set(word2)

# # for letter in unique_letters1:
# #     if letter in unique_letters2:
# #         print(letter)

# intersection = set(get_word()).intersection(get_word()).intersection(get_word())
# print(intersection)  
print("Dictionary or HashMap")

# countries = dict()
# countries["USA"] = "Washington"
# countries["Russia"] = "Moscow"

# print(countries)

# for country,capital in countries.items():
#     print("The capital of {} is {}".format(country,capital))


# for key in countries.keys():
#     print(key)

# for value in countries.values():
#     print(value)

         
# print(countries.keys())
# print(list(countries.keys()))
# print(list(countries.values()))
        
# word_counter = dict()

# word_counter["hello"] = 2

# word_counter["hello"] = 1

# word_counter["hello"] += 1


# words = dict()

# words[1] = []

# words[1].append("abc")

# print(words)

#1 Assignment: Counter
# accept the word and print how many times each letter appear

# word = "hello"
# for letter in word:
#     print(letter)


# # h : 1
# # e : 1
# # l : 2
# # o : 1

# letters = dict()

# if "a" in letters:
#     print("key a exist")
# else:
#     print("a is not in dictionary")
    
# sentence = "hello world hello world another world"

# nums = sentence.split(" ")

# frequency = dict()

# for num in nums:
#     if num not in frequency:
#         frequency[num] = 0

#     frequency[num] += 1

# print(frequency)


# accept the items person wants to buy

# and how many of each item

# ask for a price

# calculate total

# add 8.25%

check = dict()

#item name
# item price


# Creating a database
database = dict()
database["bread"] = 3
database["eggs"] = 5
database["coke"] = 12
database["beer"] = 10

def isEligble():
    age = int(input("Provide your age: "))
    return age > 17
    
def communicate_with_customer():
    card = []

    item = ""
    
    while item != "stop":
        item = input("What are you buying today: ")
        if item in database:
            if item == "beer":
                if not isEligble():
                    continue
            card.append(item)
        else:
            print("try again")

    return card



def calculate_total(items_in_card):
        
    for item in items_in_card:
        if item not in check:
            check[item] = 0
        check[item] += 1
    total = 0
    for item,count in check.items():
        total += (database[item] * count)
    total = total * 1.085
    print("Total cost for your products:{}".format(total))



calculate_total(communicate_with_customer())