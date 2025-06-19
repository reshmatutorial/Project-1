import random
import string

def generate_password(length=12, use_upper=True, use_lower=True, use_digits=True, use_special=True):
    characters = ''
    if use_upper:
        characters += string.ascii_uppercase
    if use_lower:
        characters += string.ascii_lowercase
    if use_digits:
        characters += string.digits
    if use_special:
        characters += string.punctuation

    if not characters:
        return "Please select at least one character type."

    password = ''.join(random.choice(characters) for _ in range(length))
    return password

# Example usage
password = generate_password(length=16, use_upper=True, use_lower=True, use_digits=True, use_special=True)
print("Generated Password:", password)
