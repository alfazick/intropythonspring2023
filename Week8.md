# Developing Programs: Example  Grading application
# *** Asks the user to enter exam points and turns them into grades

# *** Also the program prints the distribution of the grades as stars.

# First version, put everything inside of the main haha smart ))


# grades = list()

# while (True):
#     print("Points: ")
#     userInput = input()
#     if userInput == "":
#         break

#     score = int(userInput)

#     if (score < 0 or score > 100):
#         print("Impossible number.")
#         continue

#     grade = ""

#     if (score < 60):
#         grade = "F"
#     elif (score < 70):
#         grade = "D"
#     elif (score < 80): 
#         grade = "C"
#     elif (score < 90):
#         grade = "B"
#     else: 
#         grade = "A";

#     grades.append(grade);

# possible_grades = ["A","B","C", "D", "F"]

# dic_grades ={}
# for grade in grades:
#     if grade not in dic_grades:
#         dic_grades[grade] = 0

#     dic_grades[grade] += 1

# for grade in possible_grades:
#     if grade not in dic_grades:
#         print(grade)
#     else:
#         stars = dic_grades[grade]
#         print(grade + ": " + "*"*stars)



#Now it's time for OOP ver 2


class GradeRegister():
    def __init__(self):
        self.grades = list()

    def addGrade(self,points):
        self.grades.append(self._pointToGrade(points))

    def _pointToGrade(self,score):
        grade = ""
        if (score < 60):
            grade = "F"
        elif (score < 70):
            grade = "D"
        elif (score < 80): 
            grade = "C"
        elif (score < 90):
            grade = "B"
        else: 
            grade = "A";
        return grade;
        
    def showDistribution(self):
        possible_grades = ["A","B","C", "D", "F"]
        
        dic_grades ={}
        for grade in self.grades:
            if grade not in dic_grades:
                dic_grades[grade] = 0
        
            dic_grades[grade] += 1
        
        for grade in possible_grades:
            if grade not in dic_grades:
                print(grade)
            else:
                stars = dic_grades[grade]
                print(grade + ": " + "*"*stars)
        
        

class UserInterface:
    def __init__(self,gr):
        self.graderegister = gr

    def start(self):
        while (True):
            print("Points: ")
            userInput = input()
            if userInput == "":
                break
        
            score = int(userInput)
        
            if (score < 0 or score > 100):
                print("Impossible number.")
                continue
    
            self.graderegister.addGrade(score)

    def showStatistics(self):
        self.graderegister.showDistribution()


class MainProgram:
    def __init__(self):
        gr = GradeRegister()
        ui = UserInterface(gr)
        ui.start()
        ui.showStatistics()


MainProgram()



# Practice: Reading and writing to the file.
# Open a file for writing and create it if it doesn't exist
    f = open("textfile.txt","w+")
    
    # Open the file for appending text to the end
    # f = open("textfile.txt","a+")

    # write some lines of data to the file
    for i in range(10):
        f.write("This is line %d\r\n" % (i+1))
    
    # close the file when done
    f.close()
    
    # Open the file back up and read the contents
    f = open("textfile.txt","r")
    if f.mode == 'r': # check to make sure that the file was opened
        # use the read() function to read the entire file
        # contents = f.read()
        # print (contents)
      
        fl = f.readlines() # readlines reads the individual lines into a list
        for x in fl:
            print (x)





#print("Week8: Write vending machine application")

# 1) Part Imititate Machine
# take care of capacity
# a) load items
# b) sell items
# c) generate report

# 2) Calculate our profit and write
# inventory report into a file.

# Step 1: Create a class called Item
# class Item
# price
# Code    
# name 

# class Item:
#     def __init__(self,price,code,name):
#         self.price = price
#         self.productcode = code
#         self.name = name
#     def display_item(self):
#         print(self.price,self.productcode,self.name)
#     def __str__(self):
#         return "Item {} with code:{} costs:{}$".format(self.name,self.productcode,self.price)

# product = Item(5,777,"Dr Pepper")
# print(product)
# product.display_item()

# # Step 1) Open file 
# # # 3 mode: Write,Read,Append 
# # f = open("Week1.md","r");

# # # Step
# # content = f.read()

# # print(content)



# # Write
# # Vending Machine Class

# class VendingMachine:
#     def __init__(self,capacity):
#         self.capacity = capacity
#         self.products = list()
        
#     def add_product(self, item):
#         if len(self.products) < self.capacity:
#             self.products.append(item)
            
#     def set_capacity(self, new_capacity):
#         if new_capacity > len(self.products):
#             self.capacity = new_capacity
         
#     def generate_report(self):
#         f = open("itemReport.txt","w+")
#         for report in self.products:
#             text = "{}".format(product)
#             f.write(text)
#         f.close()


print("Week8: Back up and Recovery")
# Step 1) Writing to File
# f = open("itemReport.txt","w+")
# text = "hello"
# f.write(text)
# f.close() 

# Step 2) Reading from file 
# # 3 mode: Write,Read,Append 
# f = open("Week1.md","r");
# # Step
# content = f.read()
# print(content)
# Read  
# BackUp-Recovery 

#1) Ask user Name, Major, 
#2) ask for a filename
#3) Save that information inside file 
#4) Print the content
name = "Askar"
major = "Computer Science"
filename = "info"
text = "{}:{}\n".format(name,major)
f = open("{}.txt".format(filename),"w+")
f.write(text)
f.close()

class Student:
    def __init__(self,n,m):
        self.name = n 
        self.major = m

    def showInfo(self):
        print ("{} : {}".format(self.name,self.major))


def save_record(local_student, filename):
    text = "{}:{}\n".format(local_student.name,local_student.major)
    f = open(filename,"a+")
    f.write(text)
    f.close()

st1 = Student("John", "Physics")
# st1.showInfo()

save_record(st1,"info.txt")
def create_from_record(text):
    words = text.split(":")
    return Student(words[0],words[1])

# text = "name:major"
# st2 = create_from_record(text)
# st2.showInfo()

f = open("info.txt","r");
content = f.read()

for record in content.split("\n"):
    if not record:
        continue 
    st = create_from_record(record)
    st.showInfo()
    

