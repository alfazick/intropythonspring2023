
print("Recap")

# write a GPA calculator

#1) Write a program ask a student name, major
# ask for the student grades, till he type stop
# then print his averageGPA
# def accept_grade():
#     userInput = input("Type your grade as a letter: ").toUpper()
#     good_grades = "FDCBA"
#     # match = dict()
#     # for idx,letter in enumerate(good_grades):
#     #     match[letter] = idx 
    
#     if len(userInput) == 1 and userInput in good_grades:
#         return good_grades.index(userInput)
#     else:
#         accept_grade()
    
# grades = list()
# while len(grades) < 3:
#     grade = accept_grade()
#     grades.append(grade)

# print(grades)
    

# Write a class called Univerisity which has a list of students (each student is a seperate class)
# calculate average GPA for each student and print on the screen
# create at least 3 students you need to have two classes
# 1) University  2) Student
# University should have a list of students
# There should be a method printStatistics()
# Output: Student Name: Avg GPA :
class Student:
    def __init__(self,name):
        self.name = name 
        self.grades = list()
    def addGrade(self,grade_num):
        self.grades.append(grade_num)
    def calculateAverageGPA(self):
        total = sum(self.grades)
        return total / len(self.grades) 
    def showStudentStat(self):
        print("Student name: {} Avg GPA:{}".format(self.name,self.calculateAverageGPA()))

    def __str__ (self):
        return "Student name: {} Avg GPA:{}".format(self.name,self.calculateAverageGPA())
        
class University:
    def __init__(self):
        self.students = list()
    def add(self,student):
        self.students.append(student)
    def printStatistics(self):
        for student in self.students:
            print(student)
            student.showStudentStat()


student1 = Student("John")
student1.addGrade(4)
student1.addGrade(3)
student1.showStudentStat()

un = University()
un.add(student1)
un.printStatistics()
