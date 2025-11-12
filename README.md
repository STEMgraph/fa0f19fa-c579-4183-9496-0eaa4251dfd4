<!---
{
  "id": "fa0f19fa-c579-4183-9496-0eaa4251dfd4",
  "teaches": "Printing Runtime Values",
  "author": "Stephan Bökelmann",
  "depends_on": ["a2596a91-c7de-477a-bfbb-b08867f1aa89"],
  "first_used": "2025-03-20",
  "keywords": ["C", "exercises", "printf", "runtime values", "types"]
}
--->

# Printing Runtime Values

## 1) Introduction

In the [printf for Constant Strings](https://github.com/STEMgraph/a2596a91-c7de-477a-bfbb-b08867f1aa89?tab=readme-ov-file#printf-for-constant-strings) exercise, we introduced the `printf` function:

```C
int printf(const char* restrict format, ...);
```

At that time, we chose to avoid discussing the **ellipsis (`...`)** in detail. Now, let's explore it further. The ellipsis represents a **variadic argument pack**, meaning that `printf` can accept a variable number of additional arguments.

At first, this might seem like a wild idea, but it makes perfect sense when considering the purpose of `printf`. The function name itself hints at its functionality: it consists of **"print"** and **"f"**, where *f* stands for **format**. This means that before a string is sent to `stdout` and displayed by the terminal, `printf` processes the format string and replaces placeholders with runtime values.

This is particularly useful when variables need to be displayed in output. Placeholders are inserted into the format string, and their corresponding values are supplied as additional arguments in the function call. The function then maps these values to the respective placeholders.

### Common Format Specifiers

`printf` supports multiple format specifiers, including:

1. `%s` - String
2. `%d` - Integer (decimal)
3. `%f` - Floating point number

For a complete list of format specifiers, refer to the [cppreference documentation](https://en.cppreference.com/w/c/io/fprintf).

### 1.1) Further Readings and Other Sources

- [printf on cppreference](https://en.cppreference.com/w/c/io/fprintf)
- [CodeVault about Format Strings in C](https://youtu.be/rUA3IkQNe5I?si=0tx-oLNQunjUn2fV)

## 2) Tasks

1. **Basic Print Statements**: Write a simple program that uses `printf` to print a greeting message and your name.
2. **Printing Variables**: Declare an integer, a floating-point number, and a string. Use `printf` to display their values in a formatted output.
3. **Using Multiple Placeholders**: Create a program that prints a formatted sentence incorporating at least three different format specifiers.
4. **User Input and Output**: Write a program that asks for the user’s name and age, then prints a formatted message including these values.
5. **Calculations with Printf**: Declare two integer variables, calculate their sum and product, and display the results using `printf`.

## 3) Questions

1. Why is the `printf` function called variadic, and what does the ellipsis (`...`) in its prototype signify?
2. How does `printf` determine which values to replace in the format string?
3. What are some potential pitfalls of using incorrect format specifiers in `printf`?

## 4) Advice

Practice using `printf` with different data types and formatting options to understand its behavior. Experimenting with incorrect format specifiers can also help you learn common errors and how to debug them. Always refer to documentation for best practices in formatted output handling.
