# 1. What was the bug?
The bug was that using the '+' operator on strings concatenates them. This is why "1" + "2" became "12."

# 2. How would you fix it?
In order to fix it, I would instead initialize result in this way:
let result = Number(num1) + Number(num2);

This way, num1 and num2 are casted to numbers before being added.

```javascript
function calculateSum(num1, num2) {
    let result = Number(num1) + Number(num2);
    return result;
}