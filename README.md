# ReDI Project_Random Password Generator:
# Importing the relevant modules
# Student name: Sahar Ayubi
import string
import random

print("Hello, I am a strong password maker!")
print("Strong password utilize mixed case, number and symbols!Please select at least one option!")
# define data
number = ""
symbol = ""
lowercase_letter = ""
capital_letter = ""
# request input from user
length = int(input("Please enter password length: "))
n = input("Do you want number in your password? Press 1 for Yes and press 2 for No: ")
if n == "1":
    number = string.digits
elif n == "2":
    pass
else:
    print("Unexpected input")
s = input("Do you want symbols in your password? Press 1 for Yes and press 2 for No: ")
if s == "1":
    symbol = string.punctuation
elif s == "2":
    pass
else:
    print("Unexpected input")
lo = input("Do you want lowercase letter in your password? Press 1 for Yes and press 2 for No: ")
if lo == "1":
    lowercase_letter = string.ascii_lowercase
elif lo == "2":
    pass
else:
    print("Unexpected input")
c = input("Do you want capital letter in your password? Press 1 for Yes and press 2 for No: ")
if c == "1":
    capital_letter = string.ascii_uppercase
elif c == "2":
    pass
else:
    print("Unexpected input")
# create the password
password = "".join(random.choices(capital_letter + lowercase_letter + symbol + number, k=length))
print(password)
