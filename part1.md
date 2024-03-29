# JavaScript Fundamentals - [Part 1](https://www.theodinproject.com/courses/foundations/lessons/fundamentals-part-1) 

## 1. How do you declare a variable?
A _variable_ is a storage container for data.

```js
let message;
message = 'Hello'; //store the string
// or
let message = 'Hello';
```

## 2. What are three different ways to declare a variable?
- `var`
- `let`
- `const`

## 3. Which one should you use when?
* `var` declarations are **globaly-scoped** or **function-scoped**, and declartions are processed when the _script or function starts_. This is called **hoisting**.
JavaScript **hoists** the variable declarion to the top of the function block. `var` variables are hoisted to the top of their scope and initialized with a value of `undefined`. `var` variables can be updated and re-declared within its scope.

* `let` declarations provides **block-scoping**, `{}`, and are hoisted to the top of their scope. Unlike `var` which is initialized as `undefined`, the `let` keyword is not initialized. So if you try to use a `let` variable before declaration, you'll get a `Reference Error`. `let` variables can be updated but not re-declared.

* `const` variables are **immutable** and can _neither be updated nor re-declared_. `const` is **block scoped** and must be initialized during declaration.

Here is a link to [Hacker Noon](https://medium.com/hackernoon/why-you-shouldnt-use-var-anymore-f109a58b9b70) on why we shouldn't use var anymore.

## 4. What are the rules for naming variables?
- ⚠️ Declaring a variable twice triggers an error
- The name must contain only letters, digits, or the symbols `$` and `_`
- The first character must not be a digit
- Case matters!
- `let`, `class`, `return`, and `function` are reserved and cannot be used as variable names
- When the name contains multiple words, **camelCase** is commonly used

`"use strict";` defines that JavaScript code should be executed in "strict mode". Strict mode changes previously accepted _"bad syntax"_ into real errors.

```js
"use strict";
x = 3;       // This will cause an error because x is not declared
```

## 5. What are operators, operands, and operations?
Check out this [guide on MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) on expressions and operators.
A **binary** operator requires two operands, one before the operator and one after the operator:
`operand1` `operator` `operand2` e.g. `3 + 4` or `x * y`.
A **unary** operator requires a single operand, either before or after the operator:
`operator` `operand` OR `operand` `operator` e.g. `x++` or `++x`.


## 6. What is concatenation and what happens when you add numbers and strings together?
Concatenation is the process of appending one string to the end of another string. You can check out this [tutorial](https://masteringjs.io/tutorials/fundamentals/string-concat) on the 3 ways to concatenate strings in JavaScript.
Adding two numbers, will return the sum, but adding a number and a string will return a string.

## 7. What are the different types of operators in JavaScript?
1. Arithmetic Operators e.g. `20%10 = 0` or `let a=10; a++; Now a = 11`
2. Comparison (Relational) Operators e.g. `20!==20 = false`
3. Bitwise Operators e.g. `(10==20 & 20==33) = false`
4. Logical Operators e.g. `(10==20 && 20==33) = false`
5. Assignment Operators e.g. `var a=10; a+=20; Now a = 30`
6. Special Operators e.g. `(?:)	Conditional Ternary Operator returns value based on the condition. It is like if-else.`

## 8. What is the difference between == and ===?
`==` in JavaScript is used for comparing two variables, but it ignores the datatype of variable. `===` is used for comparing two variables, but this operator also checks datatype and compares two values.

## 9. What are operator precedence values?
This [MDN doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence) explains how operators are parsed concerning each other.

## 10. What are the increment/decrement operators?
The increment and decrement operators in JavaScript will add one (+1) or subtract one (-1), respectively, to their operand, and then return a value. This [Codeburst lesson](https://codeburst.io/javascript-increment-and-decrement-8c223858d5ed) explains that using `++` or `--` prior to our variable, the operation executes and adds/subtracts 1 prior to returning.

## 11. What is the difference between prefixing and post-fixing them?
Another useful post on [Hacker Noon](https://hackernoon.com/javascript-back-to-basics-prefix-vs-postfix-8da5256223d2) about prefix vs. postfix and the difference between them.

## 12. What are assignment operators?
Assignment operators assign values to JavaScript variables. [W3Schools](https://www.w3schools.com/js/js_assignment.asp) provides a list of the various assignment operator that can be used.

## 13. What is the **Unary +** Operator?
The unary plus operator precedes its operand and evaluates to its operand but attempts to convert it into a number, if it isn't already. Check out the [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Unary_plus) for more information.
