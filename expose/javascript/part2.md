# 1. What will happen at line 12 and why?
Line 12 prints: 3 
because var is function scoped and still exists after the for loop finishes executing. i starts at 0, then increments to 1, then 2, then the for loop is broken because 3 is not less than 3. This final value of 3 is printed on line 12.

# 2. What will happen at line 13 and why?
Line 13 prints: 150
because discountedPrice is declared using the var in the for loop. Since discountedPrice has function scope, it is still accessible outside the for loop anywhere in the discountPrices function. When prices[i] = 300 in the last iteration of the for loop, discountedPrice is 300 * (1 - 0.5) = 150. Therefore, 150 is logged to the console on line 13.

# 3. What will happen at line 14 and why?
Line 14 prints: 150
because in the final iteration of the for loop when it processed 300, discountedPrice = 150 as mentioned before and Math.round(150 * 100)/100 is 150. 150 is the finalPrice after the for loop finishes, when line 14 logs it to the console.

# 4. What will this function return and why?
The function returns: [50, 100, 150]
The function loops through prices and applies a 50% discount to each item, rounds the result, then puts the new price in the discounted array. On line 16, the full discounted array is returned.

# 5. What will happen at line 12 and why?
Line 12 will return an error because i is declared using the let keyword in the for loop block. Since "let" is block scoped, i is only accessible within the for loop. By the time line 12 is reach, i has been destroyed so the program cannot print it.

# 6. What will happen at line 13 and why?
Line 13 will return an error because discountedPrice is declared using the let keyword in the for loop block. When line 13 tries to access it, discountedPrice has already been destroyed.

# 7. What will happen at line 14 and why?
Line 14 will print: 150
because finalPrice is declared with let at the beginning of the function (in the main function block) meaning that it has scope across the entire function. At line 14, when prices[i] = 300, finalPrice is updated to 150 and line 14 can print it.

# 8. What will this function return and why?
The function will return: [50, 100, 150] because the discounted array and finalPrice and declared in the right scope. The code works as intended: it loops through the price, applies the discount, and then populates the discounted array.

# 9. What will happen at line 11 and why?
The code returns an error because i is declared using "let" in the for loop initialization. Once the for loop finishes, i is destroyed so line 11 can't access it.

# 10. What will happen at line 12 and why?
Line 12 prints: 3
because length is declared using "const" at the top of the function block. Since it's declared in the main function, it has scope over the whole function. The function was called on prices which has 3 elements, so length = 3. Line 12 can access the value of 3.

# 11. What will thsi function return and why?
The function returns: [50, 100, 150] because discounted is declared with "const" but that just stops it from being reassigned. The internal contents can still be modified. The for loop will run without any issues because a new discountedPrice variable is created at every iteration so no reassignment ever occurs. The discounted values are correctly pushed to the discountedPrice array.

# 12. Write the notation for:
## A: Accessing the value of the name property in the student object
student.name

## B. Accessing the value of the Grad Year property in the student object
student['Grad Year']

## C. Calling the function for the greeting property in the student object
student.greeting()

## D. Accessing the name property of the object in the Favorite Teacher property in student
student['Favorite Teacher']

## E. Access index zero in the array of the courseLoad property of the student object
student.courseLoad[0]

# 13. Arithmetic
## A. '3' + 2
'32' because the "+" operator does a string concatenation when one of the operands is a string. The integer maps to its exact string representation.

## B. '3' - 2
1 because the "-" operator is only for math, which forces JavaScript to convert the string '3' into the number 3 before subtracting.

## C. 3 + null
3 because `null` is mathematically evaluated as the number 0. 

## D. '3' + null
'3null' because the "+" operator with a string triggers concatenation, converting `null` into its string form.

## E. true + 3
4 because `true` maps to the number 1 in mathematical operations.

## F. false + null
0 because `false` maps to 0 and `null` maps to 0.

## G. '3' + undefined
'3undefined' because the "+" operator with a string triggers concatenation, converting `undefined` into its string form.

## H. '3' - undefined
NaN because `undefined` converts to `NaN` (Not a Number). Any math operation involving `NaN` evaluates to `NaN`.

# 14. Comparison
## A. '2' > 1
True, because the string '2' is converted into the number 2 before the numerical comparison.

## B. '2' < '12'
False, because when comparing two strings, JavaScript evaluates them lexicographically. Since '2' is greater than the first character '1', we get false.

## C. 2 == '2'
True, because  `==` automatically converts the string '2' to the number 2 before comparing them.

## D. 2 === '2'
False, because r `===` does not perform any type conversion. Since one is a number and the other is a string, they aren't deemed equal.

## E. true == 2
False, because `==` converts True to the number 1, and 1 is not equal to 2.

## F. true == Boolean(2)
True, because `Boolean(2)` evaluates to True (!= 0). Then, true = true.

# 15. Explain the difference between the == and === operators.
The loose equality `==` operator checks if two values are equal after attempting to automatically convert their data types to match. The strict equality `===` operator checks if two values are equal without performing any type conversion, so both have to be the same type of variable and have the same value.

# 17. Result of modifyArray([1,2,3], doSomething)
The result will be: [2, 4, 6].
The modifyArray function loops through the input array [1, 2, 3]. In each iteration, it calls the doSomething callback function on the current element, which multiplies the number by 2. The doubled value then gets pushed into the newArr array. Once the loop finishes, the fully populated newArr is returned.

# 19. What is the output of the above code?
The output is:
1
4
3
2
1 and 4 get printed first because they are standard synchronous `console.log` statements executed sequentially. 3 is next because it's an asynchronous callback, so it's pushed to the Web API and event queue. It has wait for the synchronous code to finish before executing. 2 is printed last because its setTimeout gives it a 1 sec delay.