# PYTHON-Assign-Q10
# Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Open the file for writing
with open("prime_600_800.txt", "w") as file:
    for num in range(600, 801):
        if is_prime(num):
            file.write(str(num) + "\n")

print("Prime numbers between 600 and 800 written to 'prime_600_800.txt'.")

