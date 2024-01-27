# A-simple-Python-script-that-takes-user-input-performs-calculations-and-displays-the-results-
# Function to perform calculations based on user input
def calculate():
    try:
        # Taking user input for numbers and operation
        num1 = float(input("Enter the first number: "))
        operator = input("Enter the operator (+, -, *, /): ")
        num2 = float(input("Enter the second number: "))

        # Performing calculations based on the operator
        if operator == '+':
            result = num1 + num2
        elif operator == '-':
            result = num1 - num2
        elif operator == '*':
            result = num1 * num2
        elif operator == '/':
            if num2 != 0:  # Check for division by zero
                result = num1 / num2
            else:
                return "Error: Division by zero!"
        else:
            return "Error: Invalid operator!"

        # Displaying the result
        return f"Result: {num1} {operator} {num2} = {result}"

    except ValueError:
        return "Error: Invalid input! Please enter valid numbers."
    except Exception as e:
        return f"An error occurred: {e}"

# Main function to execute the script
def main():
    print("Welcome to Simple Calculator!")
    print("Enter 'quit' to exit.")

    while True:
        # Calling the calculate function and displaying the result
        user_input = input("Enter calculation (e.g., 2 + 3): ")
        if user_input.lower() == 'quit':
            print("Thank you for using the calculator. Goodbye!")
            break
        else:
            print(calculate())

if __name__ == "__main__":
    main()
