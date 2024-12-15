# Python---Assignment-3
This Assignment explains about the conditional &amp; looping statements in python
#Exercise:1 Name your file: MonthNames.py
# Write a program that reads an integer value between 1 and 12 from the user and prints output the corresponding month of the year.
# An example run of the program (numbers in bold are typed in by the user) Enter the month: 3 Month 3 is March
months=("january","february","march","april","may",
        "june","july","august","september","october","november","december")
month_number=int(input("enter the month "))
if 1 <=month_number<=12:
    print("month",month_number," is " f"{months[month_number - 1]}")
else:
    print("Error:please enter a valid number between 1 and 12")

#Exercise:2 A certain cinema currently sells tickets for a full price of 6 pounds
# but always sells tickets for half price to people who are less than 16 years old, and for a third of the price for people who are 60 years old or more.
# An example run of the program (numbers in bold are typed in by the user) Enter your age: 63 Your ticket costs £2.00
age=int(input("enter your  age"))
if age<16:
    print("Your ticket costs £3.00")
elif age>=60:
    print("Your ticket costs £2.00")
else:
    print("Your ticket costs £6.00")

#Exercise 3 : Name your file: BodyMassIndex.py Write a program to calculate your BMI and give weight status.
# Body Mass Index (BMI) is an internationally used measurement to check if you are a healthy weight for your height.
# The metric BMI formula accepts weight in kilograms and height in meters:
# BMI= weight(kg)/height2(m2) BMI Weight Status Categories table BMI range - kg/m2 Category Below 18.5 Underweight 18.5 -24.9 Normal 25 - 29.9 Overweight 30 & Above Obese
# An example run of the program (numbers in bold are typed in by the user) Enter your weight in (kg): 75 Enter your height in (m): 1.70 Your BMI is: 25.95 You are in the “overweight” range.
weight=float(input("Enter your weight"))
height=float(input("Enter your height"))
BMI = weight / (height ** 2)
print(f"Your BMI is: {BMI:.2f}")
if BMI<18.5:
    print("You are in the Underweight range.")
elif 18.5<= BMI <=24.9:
    print("You are in the Normal range.")
elif 25.00<=BMI  <=29.9:
    print("You are in the Overweight range.")
else :
    print("You are in the Obese.")

# Exercise 4 : Write a Python program to receive 3 numbers from the user and print the greatest among them.
num1=float(input("enter a number1"))
num2=float(input("enter a number2"))
num3=float(input("enter a number3"))

if num1>=num2 and num1>=num3:
    print("greatest number is"" " f"{num1}")
elif num2>=num1 and num2>=num3:
    print("greatest number is"" "f"{num2}")
else:
    print("greatest number is"" "f"{num3}")

#Exercise 5 : Find the factorial of a given number using loops(note the number is received from the user)
num=int(input("Enter a number:"))
factorial=1
if num==0 or num==1:
    print("factorial is 1")
elif num<0:
    print("Enter a positive number")
else:
    for i in range(1,num+1):
     factorial=factorial*i
    print("Factorial of the number is",factorial)
# Exercise 6: Reverse a number using while loop
x=int(input("Enter a number"))
copy=x
rev=0
while(x>0):
    y=x%10
    rev=rev*10+y
    x=x//10
print("reverse of the number",copy,"is",rev)

# Exercise 7: Finding the multiples of a number using loop
x=int(input("Enter a number:"))
print("multiples of the number",x,"are:")
for i in range(1,11):
    print(i*x)
# Exercise 8: Write a program to print the inputted value as it is and break the loop if the value is 'done'.
# Example run of the program :hello there hello there :finished finished :done Done
x=input("Enter a value or(done to exit)")
while x.lower()=="done":
    break
else:
    print(x)

# Exercise 9: Write a program that prints the numbers from 1 to 10.
# But for multiples of three print "Fizz" instead of the number and for the multiple of five print "Buzz".
# For numbers which are multiples of both three and five print "FizzBuzz"
for i in range(1,11):
    if i%3==0 and i%5==0:
        print("FizzBuzz")
    elif i%5==0:
        print("Buzz")
    elif i%3==0:
        print("Fizz")
    else:
        print(i)

# Exercise 10 :Write a program to print the following pattern:
# 5 4 3 2 1
# 4 3 2 1
# 3 2 1
# 2 1
# 1
for i in range(5,0,-1):
    for j in range(i,0,-1):
       print(j,end=" ")
    print()
