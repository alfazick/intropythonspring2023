print("Decorators: Functions In Depth")

# Example 1: Calculating how long function gonna execute

import time

def timer_decorator(func):
    def wrapper(*args):
        start_time = time.time()
        result = func(*args)
        end_time = time.time()
        print(f"{func.__name__} took {end_time - start_time:.2f} seconds to execute")
        return result
    return wrapper

@timer_decorator
def slow_function(n):
    time.sleep(n)
    return n

result = slow_function(2)

# Example 2: Decorator for memoization (caching results)

def memoization_decorator(func):
    cache = {}
    
    def wrapper(*args):
        if args in cache:
            return cache[args]
        else:
            result = func(*args)
            cache[args] = result
            return result
            
    return wrapper

@memoization_decorator
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(30))


# Example 3: Decorator for logging function calls

import logging

def logging_decorator(func):
    def wrapper(*args, **kwargs):
        logging.info(f"Function '{func.__name__}' called with args: {args} and kwargs: {kwargs}")
        result = func(*args, **kwargs)
        logging.info(f"Function '{func.__name__}' returned: {result}")
        return result
    return wrapper

logging.basicConfig(level=logging.INFO)

@logging_decorator
def add(a, b):
    return a + b

result = add(3, 4)


# Example 4: Class-based decorator with arguments

class RepeatDecorator:
    def __init__(self, n):
        self.n = n
        
    def __call__(self, func):
        def wrapper(*args, **kwargs):
            for _ in range(self.n):
                result = func(*args, **kwargs)
            return result
        return wrapper

@RepeatDecorator(3)
def print_message(msg):
    print(msg)

print_message("Hello, Python!")

# Example 5: Combining decorators

import random

def emoji_decorator(func):
    emojis = ['😀', '😃', '😄', '😁', '😆', '😅', '😂']
    
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return f"{random.choice(emojis)} {result} {random.choice(emojis)}"
    return wrapper

def repeat_decorator(n):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                result = func(*args, **kwargs)
                print(result)
        return wrapper
    return decorator


@repeat_decorator(3)
@emoji_decorator
def greet(name):
    return f"Hello, {name}!"

greet("Alice")

Assignment:
Create a Python script to apply a custom greeting to a list of names using decorators to format the output

Instead of emojs use "*#", print only once
You need just one decorator




# Example 6 Advanced


import requests
import time

def rate_limit_decorator(requests_per_second):
    period = 1 / requests_per_second

    def decorator(func):
        
        def wrapper(*args, **kwargs):
            start_time = time.time()
            response = func(*args, **kwargs)
            wait_time = period - (time.time() - start_time)
            
            if wait_time > 0:
                time.sleep(wait_time)
            
            return response
        return wrapper
    return decorator

def log_response_decorator(func):
    
    def wrapper(*args, **kwargs):
        response = func(*args, **kwargs)
        print(f"API call to '{response.url}' returned status code {response.status_code}")
        return response
    return wrapper

@rate_limit_decorator(requests_per_second=2)
@log_response_decorator
def fetch_trivia_question():
    response = requests.get("https://opentdb.com/api.php?amount=1")
    return response

# Fetch 5 trivia questions
for _ in range(5):
    response = fetch_trivia_question()
    question_data = response.json()
    question = question_data['results'][0]['question']
    print(f"Question: {question}\n")

