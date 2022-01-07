# Data Types

#### Interpreting Declarations

A distinctive syntactic peculiarity of C is that declaration mirror the use of
the declared object as it would be in a normal expression.

The following set of operators with identical precedence and associativity are reused in declarators, namely:

- the unary \* "dereference" operator which denotes a pointer;
- the binary \[\] "array subscription" operator which denotes an array;
- the (1+n)-ary \(\) "function call" operator which denotes a funtion;
- the \(\) grouping parentheses which override the precedence and associativity of the rest of the listed operators.

The above three operators have the following precedence and associativity:

| Operator | Relative Precedence Associativity |
|----------|-----------------------------------|
|\[\] \(array subcription\) 1 | Left-to-right |
|\(\) \(function call \) 1 | Left-to-right |
|\* \(dereference \) 1 | Right-to-left |

When interpreting declarations, one has to start from the identifier outward and apply the adjacent operators in the correct
order as per the above table. Each application of an operator can be substituted with the following English words:

| Expression | Interpretation |
|------------|----------------|
| thing\[X\] | an array of size X of ... |
| thing \(t1, t2, t3 \) | a function taking t1, t2, t3 and returning... |
|\*thing | a pointer to... |

It follows that the beginning of the English interpretation will always start with the identifier and will end with the type
that stands on the left-hand side of the declaration.

**Examples**

```
char *names[20];
```

\[\] takes precedence over *, so the interpretation is: names is an array of size 20 of a pointer to char.

```
char (*place)[10];
```

In case of using parentheses to override the precedence, the * is applied first: place is a pointer to an array of size 10
of char.

```
int fn(long, short);
```

There is no precedence to worry about here: fn is a function taking long, short and returning int.

```
int *fn(void);
```

The \(\) is applied first: fn is a function taking void and returning a pointer to int.
