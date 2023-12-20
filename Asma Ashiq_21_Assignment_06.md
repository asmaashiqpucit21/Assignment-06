# Assignment 06: -

### 1. "Write a function named add_numbers that takes two parameters and returns their sum."
   


```python
def add_numbers(a, b):
    """
    Adds two numbers and returns the sum.

    Parameters:
    a (int or float): The first number.
    b (int or float): The second number.

    Returns:
    int or float: The sum of the two numbers.
    """
    return a + b
num1 = 8
num2 = 4
result = add_numbers(num1, num2)
print(f"The sum of {num1} and {num2} is: {result}")

```

    The sum of 8 and 4 is: 12
    




 ### 2.  "Define a function calculate_area to compute the area of a rectangle given its length and width."


```python
def calculate_area(length, width):
    """
    Computes the area of a rectangle.

    Parameters:
    length (float or int): The length of the rectangle.
    width (float or int): The width of the rectangle.

    Returns:
    float or int: The area of the rectangle.
    """
    area = length * width
    return area
rectangle_length = 15
rectangle_width = 7
area_result = calculate_area(rectangle_length, rectangle_width)
print(f"The area of the rectangle with length {rectangle_length} and width {rectangle_width} is: {area_result}")

```

    The area of the rectangle with length 15 and width 7 is: 105
    






### 3.  "Add a docstring to the calculate_area function explaining its purpose."
   


```python
def calculate_area(length, width):
    """
    Computes the area of a rectangle.

    Parameters:
    length (float or int): The length of the rectangle.
    width (float or int): The width of the rectangle.

    Returns:
    float or int: The area of the rectangle.

    Example:
    >>> calculate_area(10, 5)
    50
    """
    area = length * width
    return area

# Example usage:
rectangle_length = 10
rectangle_width = 5
area_result = calculate_area(rectangle_length, rectangle_width)
print(f"The area of the rectangle with length {rectangle_length} and width {rectangle_width} is: {area_result}")
```

    The area of the rectangle with length 10 and width 5 is: 50
    




    list



### 4.  "Create a function print_greeting that takes a name as an argument and prints a personalized greeting."
 


```python
def print_greeting(name):
    """
    Prints a personalized greeting for the given name.

    Parameters:
    name (str): The name for the personalized greeting.

    Returns:
    None
    """
    greeting = f"Hello, {name}! Welcome to the program."
    print(greeting)
user_name = "Asma"
print_greeting(user_name)
```

    Hello, Asma! Welcome to the program.
    

    

### 5. "Write a function is_prime that checks if a given number is prime."
   


```python
def is_prime(number):
    """
    Checks if a given number is prime.

    Parameters:
    number (int): The number to check for primality.

    Returns:
    bool: True if the number is prime, False otherwise.
    """
    if number <= 1:
        return False
    elif number == 2:
        return True
    elif number % 2 == 0:
        return False
    else:
        # Check for factors starting from 3 up to the square root of the number
        for i in range(3, int(number**0.5) + 1, 2):
            if number % i == 0:
                return False
        return True
test_number = 19
result = is_prime(test_number)

if result:
    print(f"{test_number} is a prime number.")
else:
    print(f"{test_number} is not a prime number.")
```



    19 is a prime number.




### 6.  "Implement a function factorial to calculate the factorial of a given number."


```python
def factorial(n):
    """
    Calculates the factorial of a given number.

    Parameters:
    n (int): The non-negative integer for which to calculate the factorial.

    Returns:
    int: The factorial of the input number.
    """
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
input_number = 7
result = factorial(input_number)
print(f"The factorial of {input_number} is: {result}")
```

    The factorial of 7 is: 5040
    

### 7. "Create a function print_pattern to print a specific pattern of stars."



```python
def print_pattern(rows):
    """
    Prints a right-angled triangle pattern of stars.

    Parameters:
    rows (int): The number of rows in the triangle.

    Returns:
    None
    """
    for i in range(1, rows + 1):
        print("*" * i)
triangle_rows = 7
print_pattern(triangle_rows)
```

    *
    **
    ***
    ****
    *****
    ******
    *******
    

### 8.    "Write a function multiply_numbers with default values for its parameters."
 


```python
def multiply_numbers(a=1, b=1):
    """
    Multiplies two numbers and returns the result.

    Parameters:
    a (int or float): The first number. Default is 1.
    b (int or float): The second number. Default is 1.

    Returns:
    int or float: The product of the two numbers.
    """
    return a * b
result_default = multiply_numbers()  # Uses default values (1 and 1)
result_custom = multiply_numbers(3, 4)  # Uses custom values (3 and 4)

print(f"Result with default values: {result_default}")
print(f"Result with custom values: {result_custom}")
```

    Result with default values: 1
    Result with custom values: 12
    

### 9.   "Define a function print_info that takes a variable number of arguments and prints them."
  


```python
def print_info(*args):
    """
    Prints the variable number of arguments.

    Parameters:
    *args: Variable number of arguments.

    Returns:
    None
    """
    for arg in args:
        print(arg)
print_info("Hello", "World", 2023, ["apple", "banana"])
Hello
World
2023
['apple', 'banana']
```

    Hello
    World
    2023
    ['apple', 'banana']
    

### 10.  "Create a function power_of_two that accepts a number and returns its square."
   

```python
def power_of_two(number):
    """
    Returns the square (power of two) of the given number.

    Parameters:
    number (int or float): The number for which to calculate the square.

    Returns:
    int or float: The square of the input number.
    """
    return number ** 2
input_number = 6
result = power_of_two(input_number)
print(f"The square of {input_number} is: {result}")
```

    The square of 6 is: 36
    

### 11.   "Define a variable inside a function and try to access it outside the function."
 

```python
def example_function():
    # Define a variable inside the function
    local_variable = "I am a local variable"

# Call the function
example_function()

# Try to access variable outside function (will result in an error)
print(local_variable)
```

    

### 12.   "Write a function that uses a variable from the enclosing scope."
   


```python
def outer_function():
    outer_variable = "I am from the outer function"

    def inner_function():
        # Access the variable from the enclosing scope (outer function)
        print("Inside inner function:", outer_variable)

    # Call the inner function
    inner_function()

    # Call the outer function
    outer_function()

```

   Inside inner function: I am from the outer function
    

### 13.  "Create a global variable and modify it inside a function."
   ]

```python
global_variable = 10

def modify_global_variable():
    # Access and modify the global variable
    global global_variable
    global_variable += 5

# Print the global variable before modification
print("Before modification:", global_variable)

# Call the function to modify the global variable
modify_global_variable()

# Print the global variable after modification
print("After modification:", global_variable)
```

    Before modification: 10
    After modification: 15
    

### 14.  "Write a lambda function to calculate the cube of a number."
   


```python
# Lambda function to calculate the cube of a number
cube = lambda x: x**3

# Example usage:
number = 6
result = cube(number)

print(f"The cube of {number} is: {result}")
```

    The cube of 6 is: 216
    

### 15.  "Use a lambda function as an argument with the map function."
  

```python
numbers = [1, 2, 3, 4, 5]

# Use a lambda function to square each number using map
squared_numbers = list(map(lambda x: x**2, numbers))

# Print the result
print("Original numbers:", numbers)
print("Squared numbers:", squared_numbers)
```

    Original numbers: [1, 2, 3, 4, 5]
    Squared numbers: [1, 4, 9, 16, 25]
    

### 16.  "Use a lambda function with the filter function to filter even numbers from a list."
   

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Use a lambda function to filter even numbers using filter
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

print("Original numbers:", numbers)
print("Even numbers:", even_numbers)
```

    Original numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    Even numbers: [2, 4, 6, 8, 10]
    

### 17.  "Apply a lambda function with the reduce function to find the product of a list."
  

```python
numbers = [1, 2, 3, 4, 5]

# Use a lambda function with reduce to find the product
product = reduce(lambda x, y: x * y, numbers)

print("Original numbers:", numbers)
print("Product of the numbers:", product)
```

    
    Original numbers: [1, 2, 3, 4, 5]
    Product of the numbers: 120
    

### 18.  "Sort a list of tuples based on the second element using a lambda function."
  

```python
tuple_list = [(1, 5), (3, 2), (2, 8), (4, 1), (5, 4)]

# Sort the list of tuples based on the second element using a lambda function
sorted_tuples = sorted(tuple_list, key=lambda x: x[1])

print("Original list of tuples:", tuple_list)
print("Sorted list of tuples based on the second element:", sorted_tuples)
```

    Original list of tuples: [(1, 5), (3, 2), (2, 8), (4, 1), (5, 4)]
    Sorted list of tuples based on the second element: [(4, 1), (3, 2), (5, 4), (1, 5), (2, 8)]
    

### 19. "Demonstrate the use of the zip function with two lists."
   

```python
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 22]

# Use zip to combine the elements of the two lists
combined_data = zip(names, ages)

# Convert the result to a list for easy printing
combined_list = list(combined_data)

print("Original lists:")
print("Names:", names)
print("Ages:", ages)
print("\nCombined list using zip:")
print(combined_list)
```

    Original lists:
    Names: ['Alice', 'Bob', 'Charlie']
    Ages: [25, 30, 22]

    Combined list using zip:
    [('Alice', 25), ('Bob', 30), ('Charlie', 22)]
   

### 20.  "Implement a generator function that generates Fibonacci numbers."
  


```python
def fibonacci_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

# Example usage:
# Generate the first 10 Fibonacci numbers
num_of_fibonacci_numbers = 10
fibonacci_gen = fibonacci_generator()

for _ in range(num_of_fibonacci_numbers):
    fibonacci_number = next(fibonacci_gen)
    print(fibonacci_number)
```

    0
    1
    1
    2
    3
    5
    8
    13
    21
    34
    

### 21. "Use a generator expression to create a sequence of squares."
  

```python
# Generator expression to create a sequence of squares
squares_generator = (x**2 for x in range(1, 6))

# Convert the generator expression to a list for easy printing
squares_list = list(squares_generator)

# Print the result
print("Sequence of squares:", squares_list)
```

    Sequence of squares: [1, 4, 9, 16, 25]

    

### 22.  "Write a function that uses the yield statement to produce a generator."
   

```python
def generate_squares(limit):
    """
    Generates squares of numbers up to the specified limit.

    Parameters:
    limit (int): The upper limit for generating squares.

    Yields:
    int: Squares of numbers from 1 to the limit.
    """
    for i in range(1, limit + 1):
        yield i**2

# Example usage:
# Generate squares up to the limit of 5
squares_generator = generate_squares(5)

# Iterate through the generator and print the squares
for square in squares_generator:
    print(square)
```

   1
   4
   9
   16
   25

### 23.  "Explain the difference between iterators and generators in Python."
  

```python
Iterator:
class MyIterator:
    def __init__(self, limit):
        self.limit = limit
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < self.limit:
            result = self.current
            self.current += 1
            return result
        else:
            raise StopIteration

# Usage
my_iter = MyIterator(5)
for i in my_iter:
    print(i)


     0
     1
     2
     3
     4


Generator:
def generate_numbers(limit):
    current = 0
    while current < limit:
        yield current
        current += 1

# Usage
my_generator = generate_numbers(5)
for i in my_generator:
    print(i)

```

    0
    1
    2
    3
    4
    

 ### 24.  "Write a Python program that includes a nested function. Inside the nested function, access a variable from the enclosing function's scope, and explain how the scope resolution works in this case."
  



```python
def outer_function():
    outer_variable = "I am from the outer function"

    def nested_function():
    # Access the variable from the enclosing scope (outer function)
      print("Inside nested function:", outer_variable)

    # Call the nested function
    nested_function()

   # Call the outer function
   outer_function()
```

    Inside nested function: I am from the outer function
    



### 25.  "Create a list of strings containing both uppercase and lowercase words. Use a lambda function with the sorted() function to sort the list in a case-insensitive manner."
   


```python
word_list = ["Apple", "banana", "Orange", "grape", "Kiwi", "Mango"]

# Sort the list case-insensitively using a lambda function
sorted_word_list = sorted(word_list, key=lambda x: x.lower())

print("Original word list:", word_list)
print("Sorted word list (case-insensitive):", sorted_word_list)
```

    Original word list: ['Apple', 'banana', 'Orange', 'grape', 'Kiwi', 'Mango']
    Sorted word list (case-insensitive): ['Apple', 'banana', 'grape', 'Kiwi', 'Mango', 'Orange']
    
    

### 26.  "Implement a generator function that yields prime numbers indefinitely. Use this generator to print the first 10 prime numbers."
   


```python
def is_prime(num):
    """Check if a number is prime."""
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def generate_primes():
    """Generate prime numbers indefinitely."""
    num = 2
    while True:
        if is_prime(num):
            yield num
        num += 1

# Example usage:
prime_generator = generate_primes()

# Print the first 10 prime numbers
for _ in range(10):
    print(next(prime_generator))

```

    2
    3
    5
    7
    11
    13
    17
    19
    23
    29


### 27.  "Write a decorator function that measures the execution time of another function. Apply this decorator to a function of your choice and print the execution time."
   


```python
import time

def measure_execution_time(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        execution_time = end_time - start_time
        print(f"Execution time of {func.__name__}: {execution_time:.6f} seconds")
        return result
    return wrapper

# Apply the decorator to a function of your choice
@measure_execution_time
def example_function():
    # Simulate some time-consuming task
    time.sleep(2)
    print("Function executed!")

# Call the decorated function
example_function()

```

    
    Function executed!
    Execution time of example_function: 2.000010 seconds



