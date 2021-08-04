*#MEAN-Stack-Interview-Questions *

**#JavaScript/NodeJs**

**Pure Function :**  Pure Function is a function (a block of code ) that always returns the same result if the same arguments are passed. It does not depend on any state, or data change during a program's execution rather it only depends on its input arguments

**Temporal Dead Zone**: Temporal Dead Zone is a behaviour that occurs with variables declared using let and const keywords.
It is a behaviour where we try to access a variable before it is initialized.
x = 23; // Gives reference error
let x;
function anotherRandomFunc(){
  message = "Hello"; // Throws a reference error
  let message;
}
anotherRandomFunc();

**call() and apply()** :  Call and apply are very similar—they invoke a function with a specified this context, and optional arguments. The only difference between call and apply is that call requires the arguments to be passed in one-by-one, and apply takes the arguments as an array.

**Observable**:
An observer is like a stream and allows you to pass at least zero or more events where the callback is needed for each event.
Observable is favored over Promise, it can emits multiple values over a time. The "Observable" is cold. It's not called until we're registered to it.
You may cancel an Observable with the unsubscribe() method, Observable provides a lot of efficient operators like map, foreach, filter, reduce, retry, retryWhen etc.

**What are the advantages of using promises instead of callbacks** : The main advantage of using promise is you get an object to decide the action that needs to be taken after the async task completes. This gives more manageable code and avoids callback hell.

**Diff promiss vs callback** : A key difference between the two is that when using the callbacks approach we would normally just pass a callback into a function which will get called upon completion to get the result of something, whereas in promises you attach callbacks on the returned promise object


**Call stack** : The call stack is used by JavaScript to keep track of multiple function calls. It is like a real stack in data structures where data can be pushed and popped and follows the Last In First Out (LIFO) principle. We use call stack for memorizing which function is running right now.

**Callback queue** :  The callback queue, as the name suggests, is a queue. Hence, functions added to it are processed in a first-in-first-out order. When the event loop in Javascript is fired, it first checks the call stack to see if it's non-empty. If so, it executes the function at the top of the stack.

**Event loop** : https://www.educative.io/edpresso/what-is-an-event-loop-in-javascript

**Lexicalscope** : A lexical scope in JavaScript means that a variable defined outside a function can be accessible inside another function defined after the variable declaration. But the opposite is not true; the variables defined inside a function will not be accessible outside that function.

**Hoisting**: In JavaScript, Hoisting is the default behavior of moving all the declarations at the top of the scope before code execution. Basically, it gives us an advantage that no matter where functions and variables are declared, they are moved to the top of their scope regardless of whether their scope is global or loca

**Closure** : A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function.

**Arrow function**: Arrow function is one of the features introduced in the ES6 version of JavaScript. It allows you to create functions in a cleaner way compared to regular functions.

**Strict Mode** : Strict Mode was a new feature in ECMAScript 5 that allows you to place a program, or a function, in a “strict” operating context. This strict context prevents certain actions from being taken and throws more exceptions. ... Strict mode prohibits some syntax likely to be defined in future versions of ECMAScript.

**Callback** : A callback is a function passed as an argument to another function.

**Callback Hell** : Callback Hell, also known as Pyramid of Doom, is an anti-pattern seen in code of asynchronous programming. It is a slang term used to describe and unwieldy number of nested “if” statements or functions. If you are not expecting your application logic to get too complex, a few callbacks seem harmless

**Node.js**: Node.js is a virtual machine that uses JavaScript as its scripting language and runs Chrome’s V8 JavaScript engine, Node.js is based on an event-driven architecture where I/O runs asynchronously making it lightweight and efficient.

**PHP and Node.js** are both used for the server side development and thus have become a competitor for each other. Below are some differences based on different parameters to understand the two and make decision between the two giants.

**Middleware** : Middleware functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

**What is REPL?**
PL in Node.js stands for Read, Eval, Print, and Loop, which further means evaluating code on the go

**What are node.js buffers?**
In general, buffers is a temporary memory that is mainly used by stream to hold on to some data until consumed.

**What does event-driven programming mean?**
An event-driven programming approach uses events to trigger various functions. An event can be anything, such as typing a key or clicking a mouse button. A call-back function is already registered with the element executes whenever an event is triggered.


**Debug node js:**
1. console.log
2. node debugger :  node inspect or node --inspect-brg


**#Angular :**

**Lazy loading** is a technique in Angular that allows us to load JavaScript components asynchronously when a specific route is activated.

**How Lazy Loading works** : Lazy Loading is loaded only when we need to start the application for the first time. If the user navigates to a new page, then the component for that page will load immediately. Lazy loading avoids the need for downloading the component each time when you visit the page.

**Singltone** : A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. ... It is used in scenarios when a user wants to restrict instantiation of a class to only one object. A singleton service is a service instance that is shared across components.


**What is RxJS** : RxJS is a library for reactive Streams which can be used to deal with asynchronous data streams and events called "Reactive Extensions for JavaScript" (RxJS).
RxJS uses JavaScript reactive programming. RxJS is very popular because it makes writing asynchronous code simple for developers.
An Observable is an object that over time and asynchronously emits multiple data values (data stream).


**Module**: Module in Angular refers to a place where you can group the components, directives, pipes, and services, which are related to the application. In case you are developing a website, the header, footer, left, center and the right section become part of a module.

**Template**: An Angular HTML template renders a view, or user interface, in the browser, just like regular HTML, but with a lot more functionality. When you generate an Angular application with the Angular CLI, the app. component. html file is the default template containing placeholder HTML.


**Components** : Components are the most basic UI building block of an Angular app. An Angular app contains a tree of Angular components. Angular components are a subset of directives, always associated with a template. Unlike other directives, only one component can be instantiated for a given element in a template.

**Difference between component and directive angular** : Components are typically used to create UI widgets. Directives is used to add behavior to an existing DOM element. Component is used to break up the application into smaller components. Directive is use to design re-usable components

**What is the difference between pure and impure pipe in angular?**:
A pure pipe is only called when Angular detects a change in the value or the parameters passed to a pipe.
An impure pipe is called for every change detection cycle no matter whether the value or parameter(s) changes.

The **async pipe** is a special kind of impure pipe that either waits for a promise to resolve to display data or subscribes to an observable to display the emitted values. The Async pipe saves boilerplate in the component code. The component doesn't have to subscribe to the async data source, extract the resolved values and expose them for binding, and have to unsubscribe when it's destroyed (a potent source of memory leaks). Let's see an example of this in action.

**Reactive forms and Template-driven forms** :Template-driven forms are asynchronous in nature, whereas Reactive forms are mostly synchronous. In a template-driven approach, most of the logic is driven from the template, whereas in reactive-driven approach, the logic resides mainly in the component or typescript code.

**reactive form**:  Reactive forms provide a model-driven approach to handling form inputs whose values change over time. How to create and update a basic form control, progress to using multiple controls in a group, validate form values, and create dynamic forms
Like:
read/write the value of the input at any point (even before the view is built)
Define advanced validation rules, including async validators (eg: check with the server whether the username entered is available while the user is filling out the rest of a registration form)
Be notified and react immediately when the value change
Access the native HTML form element
Reset the form...
If you care about unit tests (good coders should), reactive forms are significantly easier to test because they can be manipulated imperative.

**Dependency and Devdependency** The difference between these two, is that devDependencies are modules which are only required during development, while dependencies are modules which are also required at runtime.

**Interceptors** are a unique type of Angular Service that we can implement. Interceptors allow us to intercept incoming or outgoing HTTP requests using the HttpClient . By intercepting the HTTP request, we can modify or change the value of the request.

**Cross-Site Scripting** : Cross-Site Scripting (XSS) attacks are a type of injection, in which malicious scripts are injected into otherwise benign and trusted websites. XSS attacks occur when an attacker uses a web application to send malicious code, generally in the form of a browser side script, to a different end user.

































