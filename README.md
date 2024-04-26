# Password_generator
#Password Generator Challenge
import random
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']


print("Welcome to the Password Generator!")
user_letters = int(input(f"How many letters would you like in your password?\n")) 
user_symbols = int(input(f"How many symbols would you like?\n"))
user_numbers = int(input(f"How many numbers would you like?\n"))

password = []
for ch in range(1, user_letters + 1):
    password += random.choice(letters)
    
    
for ch in range(1, user_symbols + 1):
    password += random.choice(symbols)
    
    
for ch in range(1, user_numbers + 1):
    password += random.choice(numbers)
print(password)    


random.shuffle(password)
print(password)


password_s = ""
for char in password:
  password_s += char

print(f"Your password is: {password_s}")
