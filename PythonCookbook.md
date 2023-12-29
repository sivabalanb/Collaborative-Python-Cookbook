# Python Cookbook

This repository contains a collection of Python recipes and commands that can be useful for problem-solving.

1. **`collections.Counter` for Counting Elements::**
    ```python
    from collections import Counter

    # Count occurrences of elements in a list
    count_dict = Counter([1, 2, 3, 1, 2, 1]) # Result is Counter({1: 3, 2: 2, 3: 1})
    ```
2. **`collections.defaultdict` for Default Values:**


   ```python
   from collections import defaultdict

    my_dict = defaultdict(int)
    my_dict['key'] += 1
    
    list1 = [1, 2, 3]
    list2 = ['a', 'b', 'c']
    ```
3. **`zip` and `enumerate` for Iteration:**
    ```python
    # Pair elements from two lists
    pairs = zip(list1, list2)

    # Enumerate for index and value
    for index, value in enumerate(list1):
        print(index, value)
    ```
4. **`any` and `all` for Iterable Conditions:**
    ```python
    # Check if any element is True
    any_result = any(x > 5 for x in [1, 2, 6, 3])

    # Check if all elements are True
    all_result = all(x > 0 for x in [1, 2, 6, 3])
    ```
5. **`functools.partial` for Partial Function Application:**
    ```python
    from functools import partial

    # Create a function with fixed arguments
    multiply_by_2 = partial(lambda x, y: x * y, y=2)
    result = multiply_by_2(5)  # Result is 10
    ```
6. **`itertools.product` for Cartesian Product:**
    ```python
    from itertools import product

    # Generate Cartesian product of iterables
    result = list(product([1, 2], ['a', 'b'])) # Result is [(1, 'a'), (1, 'b'), (2, 'a'), (2, 'b')]
    ```

