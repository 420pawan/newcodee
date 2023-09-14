n = int(input("Enter the value of n to approximate the Golden Ratio: "))
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        a, b = 0, 1
        for _ in range(2, n + 1):
            a, b = b, a + b
        return b

def approximate_golden_ratio(n):
    if n < 2:
        return None
    fib_n = fibonacci(n)
    fib_n_minus_1 = fibonacci(n - 1)
    return fib_n / fib_n_minus_1


golden_ratio_approximation = approximate_golden_ratio(n)

if golden_ratio_approximation is not None:
    print(f"The {n}th Fibonacci number is: {fibonacci(n)}")
    print(f"The Golden Ratio approximation using the {n}th Fibonacci number is: {golden_ratio_approximation}")
else:
    print("Please enter a valid value of n (n should be >= 2)")
