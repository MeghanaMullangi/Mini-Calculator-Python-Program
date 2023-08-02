# Mini-Calculator-Python-Program
def calculator():
    print("Welcome to the Mini Calculator!")
    operations = {
        '1': add,
        '2': subtract,
        '3': multiply,
        '4': divide
    }

    while True:
        print("Available operations:")
        print("1. Addition")
        print("2. Subtraction")
        print("3. Multiplication")
        print("4. Division")
        print("5. Exit")
        choice = input("Enter your choice (1/2/3/4/5): ")

        if choice == '5':
            print("Thank you for using the Mini Calculator. Goodbye!")
            break

        operation = operations.get(choice)
        if operation:
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))
            result = operation(num1, num2)
            print("Result:", result)
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    calculator()


