# Basic Python Programs - Combined

# 1. Variables
name = "Yathinsai"
age = 20
marks = 85.5

print("1. Variables")
print("Name:", name)
print("Age:", age)
print("Marks:", marks)

# 2. Arithmetic Operators
a = 10
b = 5

print("\n2. Arithmetic Operators")
print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Modulus:", a % b)

# 3. User Input
print("\n3. User Input")
user_name = input("Enter your name: ")
user_age = int(input("Enter your age: "))

print("Hello", user_name)
print("Your age is", user_age)

# 4. Addition of Two Numbers
print("\n4. Addition of Two Numbers")
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

sum = num1 + num2
print("Sum =", sum)

# 5. Relational Operators
print("\n5. Relational Operators")
x = 10
y = 20

print("x > y:", x > y)
print("x < y:", x < y)
print("x == y:", x == y)
print("x != y:", x != y)

# 6. Assignment Operators
print("\n6. Assignment Operators")
value = 10

value += 5
print("After += :", value)

value -= 3
print("After -= :", value)

value *= 2
print("After *= :", value)

# 7. Area of Circle
print("\n7. Area of Circle")
radius = float(input("Enter radius: "))

area = 3.14 * radius * radius
print("Area of circle =", area)

# 8. Simple Interest
print("\n8. Simple Interest")
p = float(input("Enter principal amount: "))
r = float(input("Enter rate of interest: "))
t = float(input("Enter time: "))

si = (p * r * t) / 100

print("Simple Interest =", si)





# Simple Calculator and Area Calculation

print("----- SIMPLE CALCULATOR -----")

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

print("\nChoose an operation:")
print("1. Addition")
print("2. Subtraction")
print("3. Multiplication")
print("4. Division")

choice = int(input("Enter your choice: "))

if choice == 1:
    print("Result =", a + b)

elif choice == 2:
    print("Result =", a - b)

elif choice == 3:
    print("Result =", a * b)

elif choice == 4:
    if b != 0:
        print("Result =", a / b)
    else:
        print("Cannot divide by zero")

else:
    print("Invalid choice")


print("\n----- AREA CALCULATION -----")

print("1. Circle")
print("2. Rectangle")
print("3. Triangle")

choice = int(input("Enter your choice: "))

if choice == 1:
    radius = float(input("Enter radius: "))
    area = 3.14 * radius * radius
    print("Area of Circle =", area)

elif choice == 2:
    length = float(input("Enter length: "))
    breadth = float(input("Enter breadth: "))
    area = length * breadth
    print("Area of Rectangle =", area)

elif choice == 3:
    base = float(input("Enter base: "))
    height = float(input("Enter height: "))
    area = 0.5 * base * height
    print("Area of Triangle =", area)

else:
    print("Invalid choice")
    
    
    
    
    import random

print("----- NUMBER GUESSING GAME -----")

number = random.randint(1, 100)

while True:
    guess = int(input("Guess a number between 1 and 100: "))

    if guess < number:
        print("Too low! Try again.")

    elif guess > number:
        print("Too high! Try again.")

    else:
        print("Congratulations! You guessed the correct number.")
        break
    
    
    
    
    
    # Prime Number, Factorial and Fibonacci Series

# 1. Prime Number
print("----- PRIME NUMBER -----")

n = int(input("Enter a number: "))

if n <= 1:
    print("Not a prime number")
else:
    prime = True

    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

    if prime:
        print(n, "is a prime number")
    else:
        print(n, "is not a prime number")


# 2. Factorial
print("\n----- FACTORIAL -----")

num = int(input("Enter a number: "))
fact = 1

for i in range(1, num + 1):
    fact = fact * i

print("Factorial of", num, "=", fact)


# 3. Fibonacci Series Using Recursion
print("\n----- FIBONACCI SERIES -----")

terms = int(input("Enter number of terms: "))

def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

print("Fibonacci Series:")

for i in range(terms):
    print(fibonacci(i), end=" ")
    
    
    
    # Contact Book using Lists and Dictionaries

contacts = []

while True:
    print("\n----- CONTACT BOOK -----")
    print("1. Add Contact")
    print("2. View Contacts")
    print("3. Search Contact")
    print("4. Delete Contact")
    print("5. Exit")

    choice = int(input("Enter your choice: "))

    # Add Contact
    if choice == 1:
        name = input("Enter name: ")
        phone = input("Enter phone number: ")

        contact = {
            "name": name,
            "phone": phone
        }

        contacts.append(contact)
        print("Contact added successfully!")

    # View Contacts
    elif choice == 2:
        if len(contacts) == 0:
            print("No contacts found.")
        else:
            print("\nContacts:")
            for contact in contacts:
                print("Name:", contact["name"])
                print("Phone:", contact["phone"])
                print("----------------")

    # Search Contact
    elif choice == 3:
        name = input("Enter name to search: ")

        found = False

        for contact in contacts:
            if contact["name"].lower() == name.lower():
                print("Name:", contact["name"])
                print("Phone:", contact["phone"])
                found = True
                break

        if not found:
            print("Contact not found.")

    # Delete Contact
    elif choice == 4:
        name = input("Enter name to delete: ")

        found = False

        for contact in contacts:
            if contact["name"].lower() == name.lower():
                contacts.remove(contact)
                print("Contact deleted successfully!")
                found = True
                break

        if not found:
            print("Contact not found.")

    # Exit
    elif choice == 5:
        print("Exiting Contact Book...")
        break

    else:
        print("Invalid choice!")
        
        
        
        
        
        # Student Grading System and Frequency Counter

# 1. Student Grading System

print("----- STUDENT GRADING SYSTEM -----")

students = {}

n = int(input("Enter number of students: "))

for i in range(n):
    name = input("Enter student name: ")
    marks = float(input("Enter marks: "))

    if marks >= 90:
        grade = "A"
    elif marks >= 75:
        grade = "B"
    elif marks >= 60:
        grade = "C"
    elif marks >= 40:
        grade = "D"
    else:
        grade = "F"

    students[name] = {
        "marks": marks,
        "grade": grade
    }

print("\nStudent Details:")

for name, details in students.items():
    print("Name:", name)
    print("Marks:", details["marks"])
    print("Grade:", details["grade"])
    print("----------------")


# 2. Frequency Counter Using Dictionary

print("\n----- FREQUENCY COUNTER -----")

numbers = input("Enter numbers separated by spaces: ").split()

frequency = {}

for number in numbers:
    if number in frequency:
        frequency[number] += 1
    else:
        frequency[number] = 1

print("\nFrequency of each number:")

for number, count in frequency.items():
    print(number, ":", count)
# yathinsai
