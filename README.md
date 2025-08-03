# Python-Based-Simple-Calculator-Program
A Python-based Simple Calculator featuring modular functions for addition, subtraction, multiplication, and division with division-by-zero handling. It uses a menu-driven interface, continuous loop execution, and input validation, ensuring accuracy, usability, and clean, maintainable code

code:

    def add(x, y):
    return x + y

    def subtract(x, y):
    return x - y

    def multiply(x, y):
    return x * y

    def divide(x, y):
        if y == 0:
            return "Error! Division by zero."
        return x / y


    print("Simple Calculator")
    print("Select operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")

    while True:
        choice = input("\nEnter choice (1/2/3/4 or 'q' to quit): ")

    if choice.lower() == 'q':
        print("Exiting calculator. Goodbye!")
        break

    if choice in ('1', '2', '3', '4'):
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input! Please enter numbers only.")
            continue

        if choice == '1':
            print(f"Result: {num1} + {num2} = {add(num1, num2)}")
        elif choice == '2':
            print(f"Result: {num1} - {num2} = {subtract(num1, num2)}")
        elif choice == '3':
            print(f"Result: {num1} * {num2} = {multiply(num1, num2)}")
        elif choice == '4':
            print(f"Result: {num1} / {num2} = {divide(num1, num2)}")
    else:
        print("Invalid choice! Please choose a valid option.")
