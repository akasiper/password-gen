import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("the Password Gen")
nr_letters= int(input("How many letters would you like in your password?"))
nr_symbols = int(input(f"How many symbols would you like?"))
nr_numbers = int(input(f"How many numbers would you like?"))


nr_letters = int(input("How many letters would you like in your password?"))
nr_symbols = int(input("How many symbols would you like?"))
nr_numbers = int(input("How many numbers would you like?"))

password_list = []

password_list.extend(random.choices(letters, k=nr_letters))
password_list.extend(random.choices(symbols, k=nr_symbols))
password_list.extend(random.choices(numbers, k=nr_numbers))

random.shuffle(password_list)

password = ''.join(password_list)

print(f"Your password is: {password}")
