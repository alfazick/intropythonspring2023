
#Warm-UP

#Calculate Statistics of drawing 2 6 sided dices for million draws



# Intro to Class: Data Encapsulation
class Item:
    def __init__(self,name,price):
        self.name = name
        self.price = price
    
    def apply_discount(self,discount):
        # calculate and return price after applying discount
        return self.price * (1 - (discount/100))


    def __str__(self):
        return "Item name: " + self.name + " Price: " + str(self.price)


class ShoppingCart:
    def __init__(self):
        self.basket = []

    def addItem(self,item):
        self.basket.append(item)

    def showItems(self):
        print("Your basket has next items: ")
        for item in self.basket:
            print(item)





# Bank Account
# Create a new BankAccount class
# Perform witdraw and deposit command

























# import random


# dic_nums = dict()

# for i in range(1000000):
#     total = random.randint(1,6) + random.randint(1,6)
#     if total not in dic_nums:
#         dic_nums[total] = 0

#     dic_nums[total] +=1

# total_draws = 1000000
# for num, freq in dic_nums.items():
#     print(num,"appeared ", freq/total_draws, "procent")


print("Week 7: Intro to OOP:Class ")

# Warm up
# import random
# frequency = dict()
# for _ in range(1000000):
#     total = random.randint(1,6) + random.randint(1,6)
#     if total not in frequency:
#         frequency[total] = 0

#     frequency[total] +=1

# print(frequency)

# total = 1000000

# for num,freq in frequency.items():
#     print("{} appears with {} chance".format(num,freq/total*100))



# Assignment: Create class Book with name,author, pages:
# implement two methods to print info about the book
class Student:
    def __init__(self,name,major):
        self.name = name
        self.major = major

    def printInfo(self):
        print(self.name,self.major)

    def __str__(self):
        return "My a name is :{} I am majoring in {}".format(self.name,self.major)
        
engineer_student = Student("EE","Mechanical")
#engineer_student.printInfo()
print(engineer_student)


print("Week 7: Intro to OOP:Class ")

# Warm up

# Communicate with user ask for 3 items(name and price)
# Append each one to the list
# Print on the screen each item along with price

class Item:
    def __init__(self,name,price):
        self.name = name
        self.price = price

    def get_price(self):
        return self.price
    def __str__(self):
        return "The {} cost: {} $".format(self.name,self.price)
    def calculate_tax(self,taxRate):
        return self.price * taxRate/100
    def get_item(self):
        return "The {} cost: {} $".format(self.name,self.price)
        
class ShoppingCard:
    def __init__(self):
        self.items = list()

    def getSize(self):
        return len(self.items)

    def addItem(self,item):
        self.items.append(item)

    def calculate_total(self,taxRate):
        total = 0  
        for item in self.items:
            total += item.get_price() + item.calculate_tax(taxRate)
        return total
        
myItems = ShoppingCard()
while myItems.getSize() < 2:
    name = input("What do you want: ")
    cost = int(input("How much it cost?"))
    myItem = Item(name,cost)
    myItems.addItem(myItem)

print(myItems.calculate_total(30))
