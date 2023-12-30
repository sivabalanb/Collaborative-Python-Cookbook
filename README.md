# Leetcode Python Cookbook

This repository contains a collection of Python recipes and commands that can be useful for problem-solving.

1. **`collections.Counter` for Counting Elements:**
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

## Data Structures and Algorithms
1. **Unpacking a Sequence into Separate Variables:**

    ```python
    values = (1, 2, 3)
    a, b, c = values # Output: 1 2 3
    ```

2. **Unpacking Elements from Iterables of Arbitrary Length:**

    ```python
    def unpack_elements(iterable):
        first, *rest = iterable
        return first, rest
    
    result = unpack_elements([1, 2, 3, 4, 5])
    print(result)  # Output: (1, [2, 3, 4, 5])
    ```

3. **Keeping the Last N Items:**

    ```python
    from collections import deque

    def keep_last_n_items(iterable, n):
        items = deque(iterable, maxlen=n)
        return items
    
    result = keep_last_n_items([1, 2, 3, 4, 5], 3)
    print(result)  # Output: deque([3, 4, 5], maxlen=3)
    ```

4. **Finding the Largest or Smallest N Items:**

    ```python
    import heapq

    def find_largest_n_items(iterable, n):
        largest_items = heapq.nlargest(n, iterable)
        return largest_items

    result = find_largest_n_items([10, 2, 8, 7, 5], 3)
    print(result)  # Output: [10, 8, 7]
    ```
5. **Mapping Keys to Multiple Values in a Dictionary:**

    ```python
    from collections import defaultdict

    def map_keys_to_multiple_values():
        d = defaultdict(list)
        d['a'].append(1)
        d['a'].append(2)
        d['b'].append(3)

        print(d)  # Output: defaultdict(<class 'list'>, {'a': [1, 2], 'b': [3]})
    ```
6. **Keeping Dictionaries in Order:**

    ```python
    from collections import OrderedDict

    def keep_dictionaries_in_order():
        d = OrderedDict()
        d['foo'] = 1
        d['bar'] = 2
        d['spam'] = 3

        print(d)  # Output: OrderedDict([('foo', 1), ('bar', 2), ('spam', 3)])
    ```

7. **Calculating with Dictionaries:**

    ```python
    prices = {'apple': 1.99, 'banana': 0.99, 'orange': 2.49}
    items = [('apple', 2), ('banana', 3), ('orange', 1)]

    total_cost = sum(prices[key] * quantity for key, quantity in items)
    print(total_cost)  # Output: 9.94
    ```

8. **Finding Commonalities in Two Dictionaries:**

    ```python
    dict1 = {'a': 1, 'b': 2, 'c': 3}
    dict2 = {'b': 2, 'c': 4, 'd': 5}

    common_keys = set(dict1.keys()) & set(dict2.keys())
    print(common_keys)  # Output: {'b', 'c'}
    ```
