## Var, Let and Const

### Var

- Function Scoped: Variables declared with var are function-scoped or globally scoped.
- Hoisting: Variable declarations are hoisted to the top of their containing function or script, but not their assignments.
- Re-Declaration: Allows re-declaration of the same variable within the same scope.
- No Block Scope: var does not have block-level scope, meaning it's accessible even outside of blocks like if statements or loops.

### Let

- Block Scoped: Variables declared with let are block-scoped, meaning they only exist within the block they are defined in.
- Hoisting: Like var, variable declarations are hoisted to the top of their containing block, but not their assignments.
- No Re-Declaration: Cannot be re-declared within the same scope.
  Reassignment: Allows reassignment of the variable's value.

### Const

- Block Scoped: Like let, const is block-scoped.
- No Re-Assignment: Variables declared with const must be assigned a value when declared and cannot be reassigned a new value. However, for objects and arrays declared with const, their properties or elements can still be modified.
- No Re-Declaration: Similar to let, const cannot be re-declared within the same scope.
