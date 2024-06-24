import random
import string
import time

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(characters) for _ in range(length))

def main():
    while True:
        # Get input from the user
        try:
            length = int(input("Enter the number of digits for the password: "))
        except ValueError:
            print("Invalid input. Please enter a valid number.")
            continue
        
        # Generate and print the password
        password = generate_password(length)
        print(f"Generated password: {password}")
        
        # Sleep for 1 minute
        time.sleep(60)

if _name_ == "_main_":
    main()
