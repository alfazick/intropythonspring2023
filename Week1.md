1) Accepting Input From user
input() is a built-in function to accept input from a user, takes a string as an argument, to show the message
s = input("enter an integer: ")

3) A bit more about format printer
Pure string concatenation


Using format for strings, very nice approach usually
Just by order
s = "{0}{1}{2}".format("Gold","Silver","Bronze")
By name
s = "{who} turned {age} this year".format(who = "She", age = 100)



3) Variables and data types (e.g. strings, integers, floats, booleans)
   Good idea to check type, before starting to work with the data
   type()
   
4)Basic arithmetic operations (e.g. addition, subtraction, multiplication, division) Extra: Modular

5) Most surprising idea, specific to Python
   print(word * 5)


Code from class:

#1) Accepting Input From user
#input() is a built-in function to accept input from a #user, takes a string as an argument, to show the message
#s = input("enter an integer: ")

# print("Wait for input")
# name = input("Please type your name: ")
# print("After input accepted")
# print("Hello {}".format(name))

# print(type(name))

# int float

# x = 777
# y = 111
# temperature = 70.5

# name = "Hello"
# print(type(x))
# print(type(temperature))
# print(type(name))

# myNum = int("111")
# print(y*5)
# print(myNum*5)

# print("Welcome to my Super  calculator")

# #intermediate
# # num1 = input("Please type a first number")
# # num2 = input("Please type a second number")

# #print(eval("(5+5)*(5/10)"))


# operation = input("Please type math operation")
# num1 = 5
# num2 = 10

# expression = "{}{}{}".format(num1,operation,num2)
# result = eval(expression)

# print("Result of {}{}{} = {}".format(num1,operation,num2,result))



# num1 = int(num1)
# num2 = int(num2)


# print("Multiplication {} * {} = {}".format(num1, num2, num1 * num2))
# print("Division {} / {} = {}".format(num1, num2, num1 / num2))
# print("Addition {} + {} = {}".format(num1, num2, num1 + num2))
# print("Subtraction {} - {} = {}".format(num1, num2, num1 - num2))


# isWeatherGood = True
# doItired = False

# print(type(isWeatherGood))

# print(type(doItired))
