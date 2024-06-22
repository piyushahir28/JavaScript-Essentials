### Operator Precedence and Associativity

Operator precedence determines how operators are parsed concerning each other. Operators with higher precedence become the operands of operators with lower precedence.

### Precedence and associativity

Consider an expression describable by the representation below, where both OP1 and OP2 are fill-in-the-blanks for OPerators.

```javascript
a OP1 b OP2 c
```

The combination above has two possible interpretations:

```javascript
(a OP1 b) OP2 c
a OP1 (b OP2 c)
```

Which one the language decides to adopt depends on the identity of OP1 and OP2.

If OP1 and OP2 have different precedence levels (see the table below), the operator with the higher precedence goes first and associativity does not matter. Observe how multiplication has higher precedence than addition and executed first, even though addition is written first in the code. Within operators of the same precedence, the language groups them by associativity. Left-associativity (left-to-right) means that it is interpreted as (a OP1 b) OP2 c, while right-associativity (right-to-left) means it is interpreted as a OP1 (b OP2 c)

**Operators are first grouped by precedence, and then, for adjacent operators that have the same precedence, by associativity.**
