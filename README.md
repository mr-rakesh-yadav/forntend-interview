# frontend-interview
Frontend Interview Questions  🌐 - This is a repository focused on interview questions for 

>> Here are questions with sample answers. You can also contribute to this by editing this file. I hope we can learn together to

## 1. Please Introduce your self.
   
*__Sample-1:__*
>
I'm [Your Name], a skilled front-end developer with 2.3 years of hands-on experience in building seamless user interfaces. Currently, I'm contributing my skills and expertise at [Company Name], where I specialize in React, Javascript, Typescript, HTML, CSS, etc. 

Since the last 2.3 years, I have worked on 3 projects [Project -1], [Project -2] and [Project -1]. And My Recent/current project is [Project Name], [About Project].

My current roles and responsibilities involve UI development and optimization, ensuring visually appealing interfaces, and enhancing overall performance. Through cross-functional collaboration, I've played a key role in delivering better code quality, streamlining the development process, and integrating CI/CD practices for efficient releases.

I am excited about the prospect of bringing my experience to [Company Name] and being a valuable asset to your team.


*__Sample-2:__*
>
I'm a front-end developer with five years of experience in web development. I've worked on a variety of projects for clients in the retail, travel, and healthcare industries. I'm passionate about creating great user experiences and have a strong understanding of usability and accessibility standards.

## 2. What happens when the user enters a URL?

*__Sample-1__*
>
 When the user enters a URL into their browser, the browser sends a request to the server hosting the website. The server then sends back a response that includes the HTML for the page. The browser then renders the page based on this HTML.

*__Sample-2__*
>
When the user enters a URL into their browser, the browser involves these processes to render web-page such as - Parsing of URL, Identifying DNS to obtain IP address of domain, Establishing HTTP/HTTPS Connection, Send Request to the server, and sending a response back to the client/browser, the browser receives the response and final render the response.

## 3. How will you differentiate between == and ===?
*__Sample-1__*
>
The `===` operator is the strict equality operator, and it does not perform type coercion. I have used it in the scenario where I wanted to check its value/data as well as its type.
Whereas the `==` operator does not perform strict checks and performs type coercion.

## 4. What is CSS float property and how does it work?
*__Sample-1__*
>
The CSS float property is used to define the alignment of an element along the `left` or `right` side of its containing element, allowing other elements to flow around it. I have used it in situations like I wanted to put a particular element to the right side or the left side of the container.

## 5. What are the 3 most important languages for front-end web development?
*__Sample-1__*
>
HTML, CSS, and JavaScript are the three most important languages for front-end web development. I use these languages on a daily basis to create web applications and UI components.

## 6. What is the difference between http and https protocol?
*__Sample-1__*
>
The `https` protocol is a secure version of the `http` protocol. It encrypts all data sent between the server and the browser to prevent hackers from intercepting it. `https` operates over `port 443` by default, whereas `http` is operated over `port 80`.

## 7. What is hoisting in JavaScript?
*__Sample-1__*
>
Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their scope during the compilation phase.

## 8. How does event delegation work in JavaScript?
*__Sample-1__*
>
Event delegation is a technique in which we attach an event listener to a parent element instead of individual child elements. Events that occur on the child elements are handled by the parent element.
>
Example:
>
          document.querySelector('.parent')
                  .addEventListener('click', function(event) {
                       if (event.target.classList.contains('child')) {
                           console.log('Child element clicked!');
                       }
          });


## 9. What is the significance of closures in JavaScript with example?
*__Sample-1__*
>
Closures or Scope-chaining in JavaScript allow functions to access variables from their outer lexical environment, even after the outer function has finished executing. This helps in creating private variables, implementing data encapsulation, and maintaining state in functional programming.

* Example:

```
function createCounter(){
   let count = 0;
   function increment(){
      count++;
      return count;
   }

   function decrement(){
      count--;
      return count;
   }

   function getCount(){
      return count;
   }

   return {
        increment: increment,
        decrement: decrement,
        getCount: getCount
    };
}

// Creating a 'counter' instance
const counter = createCounter();

console.log(counter.increment()); // Outputs: 1
console.log(counter.increment()); // Outputs: 2
console.log(counter.decrement()); // Outputs: 1
console.log(counter.getCount()); // Outputs: 1

```

## 10. Explain the concept of prototypal inheritance in JavaScript?
*__Sample-1__*
>
Prototypal inheritance is a feature of JavaScript that allows objects to inherit properties and methods from other objects. Every object in JavaScript has a prototype property, and when a property or method is accessed on an object, JavaScript looks for it in the object itself and then in its prototype chain.

>>

## 11. What is hoisting and the benefits of hoisting?
*__Sample-1__*
>
Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase, regardless of where they are declared in the code.
The benefits of the hoisting are:
- Flexibility: Hoisting allows you to use variables and functions before they are declared in code. This is useful for organizing your code logically without having to worry about the order of declaration.
- Variable Scope Clarity/Visibility: Hoisting helps clarify the scope of variables. In JavaScript, variables declared with var are function-scoped rather than block-scoped. Hoisting ensures that variables declared within a function are accessible throughout the function's scope.

```
1.
console.log(x); // No error, variable x is hoisted
var x = 10;

2.
foo(); // No error, function foo is hoisted
function foo() {
    console.log('Hello from foo');
}
```

## 12. What are the types of scope in Javascript?
*__Sample-1__*
>
There are 3 types of scope -
1. Global Scope
- Variables declared outside of any function, including those declared at the top level of a script file, have global scope.
- Global variables are accessible from anywhere within the script, including within functions.

2. Local Scope:
- Variables declared inside a function have local scope.
- Local variables are only accessible within the function in which they are declared.As they create its own scope, so are not accessible from outside the function.
- Give 'ReferenceError: <variable> is not defined' error when we try to access before the declaration.

3. Block Scope:
- Variables declared using 'let' or 'const' within a block '(enclosed in curly braces {})' have block scope.
- Block-scoped variables are only accessible within the block in which they are declared.
- This includes variables declared within if, for, while, and switch statements.

## 13. What is an IIFE and it's benefits?
*__Sample-1__*
>
Immediately Invoked Function Expression, is a JavaScript function that is declared and invoked immediately after its declaration. It's defined using a function expression rather than a function declaration.
```
Syntax:
(function() {
    // logic of the code...
})();
```
There are two components of an IIFE:
- Function Expression: An IIFE is created using a function expression, which is a way of defining a function without giving it a name. This is achieved by wrapping the function definition inside parentheses `( )`.
- Invocation: Immediately after the function expression, the function is invoked by adding a pair of parentheses '( )'. This triggers the execution of the function immediately after its definition.

Benefits of IIFE:
1. Encapsulation
2. Avoiding Naming Collisions
Use Case:
- Perform some configurations of operation after the script is loaded.


## 14. What is Callback?

## 15. What is asyncronous and syncronous in js.

## 16. What is Promise and why we need it?

## 17. can we use Promises to handle synchronous and asynchronous functions in JavaScript?

## 18. What are 'promise ladder', 'promise chaining' and 'nested promise chaining'? Explain With Example.

## 19. What is async/await and Why we need it?
