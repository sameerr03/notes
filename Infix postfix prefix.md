Infix expressions: Operators are between the operands. A+B
prefix expressions: Operators are before the operands. +AB
postfix expressions: Operators are after the operands. AB+

### Conversion
Uses stack.

#### Infix to postfix
Operands go directly to the output
Operators are stored in the stack. Rules
- High priority operators cannot be before low priority - ^,(multiplication asterisk)/,+-
- Same priority cannot be together
- Whatever is in the brackets is popped
(A+B)xC/D
|Input|Stack|Output|
|---|---|---|
|(|(||
|A|(|A|
|+|(+|A|
|B|(+|AB|
|)||AB+|
|x|x|AB+|
|C|x|AB+C|
|/|/|AB+Cx|
|D|/|AB+CxD|
Final expression: AB+CxD/

#### Infix to prefix
Reverse the expression (swap parenthesis for the other type)
convert to postfix
reverse the final output
(A+B)xC/D
Reversed: D/Cx(B+A)
|Input|Stack|Output|
|---|---|---|
|D||D|
|/|/|D|
|C|/|DC|
|x|x|DC/|
|(|x(|DC/|
|B|x(|DC/B|
|+|x(+|DC/B|
|A|x(+|DC/BA|
|)|x|DC/BA+|
reversed final expression: DC/BA+x
Final expression: x+AB/CD

