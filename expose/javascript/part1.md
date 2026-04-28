# 1. Line 9 prints: 
values added: 20

# 2. Line 13 prints: 
final result: 20

# 3. Why should you not use var?
We shouldn't use var here because variables declared with var are visible through blocks and can lead to weird scoping bugs.

# 4. Line 9 prints:
values added: 20

# 5. Line 13 prints:
ReferenceError: result is not defined
This is because we declared result inside the if block. "Let" is block-scoped meaning that the result variable is not accessible after exiting the if statement. Line 13 throws an error when trying to access result because it cannot find it in the outer function's scope.

# 6. Line 9 prints:
We get an error because result was declared using const, so it can't be reassigned. Since it's initialized to 0 initially, and the code tries to reassign it to 20 on line 7, we get an error even before reaching line 9.

# 7. Line 13 prints:
We get an error here as well because const is also block scoped. The result variable only exists inside the if block and can't be seen by line 13.

