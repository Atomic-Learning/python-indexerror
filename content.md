An `IndexError`{.python} occurs when you try to access an index that doesn't exist in a sequence like a list or string. Understanding when and why this error happens is crucial for working with indexed data.

# What Causes an IndexError?

IndexError is raised when you use an index (position number) that is outside the valid range for a list or string:

```py-cell
my_list = [1, 2, 3]
print(my_list[10])
```

In this example, the list only has indices 0, 1, and 2 (three items), so trying to access index 10 raises an `IndexError: list index out of range`{.python}.

# Understanding Valid Indices

For a list or string with `n`{.python} items:

* Valid indices range from `0`{.python} to `n-1`{.python}

* Negative indices range from `-1`{.python} to `-n`{.python}

* Any index outside these ranges causes an IndexError

```py-cell
colors = ["red", "green", "blue"]
# Valid indices: 0, 1, 2 (or -3, -2, -1)

print(colors[0])    # red (valid)
print(colors[-1])   # blue (valid)
print(colors[3])    # IndexError (out of range)
```

# IndexError with Strings

Strings work the same way:

```py-cell
word = "hello"
print(word[0])      # h
print(word[4])      # o
print(word[10])     # IndexError: string index out of range
```
