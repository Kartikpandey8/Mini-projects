import math

history = []

def add(*numbers):
    return sum(numbers)

def subtract(*numbers):
    if len(numbers) > 1:
        result = numbers[0]
        for num in numbers[1:]:
            result -= num
        return result
    else:
        return "Error: At least two numbers are required for subtraction."

def multiply(*numbers):
    result = 1
    for num in numbers:
        result *= num
    return result

def divide(*numbers):
    if len(numbers) > 1:
        result = numbers[0]
        for num in numbers[1:]:
            if num != 0:
                result /= num
            else:
                return "Error: Cannot divide by zero."
        return result
    else:
        return "Error: At least two numbers are required for division."

def exponentiate(x, y):
    return x ** y

def square_root(x):
    return math.sqrt(x)

def modulus(x, y):
    if y != 0:
        return x % y
    else:
        return "Error: Cannot calculate modulus with zero divisor."

def sin_func(angle):
    return math.sin(math.radians(angle))

def cos_func(angle):
    return math.cos(math.radians(angle))

def tan_func(angle):
    return math.tan(math.radians(angle))

def display_history():
    if history:
        print("Calculation History:")
        for entry in history:
            print(entry)
    else:
        print("No calculation history.")

def calculator():
    expression = input("Enter a mathematical expression: ")

    try:
        result = eval(expression, {"__builtins__": None}, {"sqrt": square_root, "sin": sin_func, "cos": cos_func, "tan": tan_func})
        print(f"Result: {result}")

        if isinstance(result, (int, float)):
            history.append(f"{expression} = {result}")

    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    while True:
        calculator()
        another_calculation = input("Do you want to perform another calculation? (y/n): ").lower()
        if another_calculation != 'y':
            display_history()
            break
