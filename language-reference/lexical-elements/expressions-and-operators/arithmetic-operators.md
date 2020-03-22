# Arithmetic Operators

Sodium provides operators for standard arithmetic operations: addition, subtraction, multiplication, and division, along with modular division and negation. Usage of these operators is straightforward; here are some examples:

Addition

```text
x = 5 + 3;
y = 10.23 + 37.332; 
```

Subtraction

```text
x = 5 - 3;
y = 57.223 - 10.903; 
```

You can add and subtract memory pointers, but you cannot multiply or divide them.

Multiplication

```text
x = 5 * 3; 
y = 47.4 * 1.001; 
```

Division

```text
x = 5 / 3;
y = 940.0 / 20.2; 
```

You use the modulus operator % to obtain the remainder produced by dividing its two operands. You put the operands on either side of the operator, and it does matter which operand goes on which side: 3 % 5 and 5 % 3 do not have the same result. The operands must be expressions of a primitive data type.

Modular division

```text
x = 5 % 3;
y = 74 % 47; 
```

Modular division returns the remainder produced after performing integer division on the two operands. The operands must be of a primitive integer type.

Negation

```text
int x = -5; 
```

