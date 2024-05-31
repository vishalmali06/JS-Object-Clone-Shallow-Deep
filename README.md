 # JavaScript Copy Examples
 
    This repository demonstrates the difference between shallow copy and deep copy in JavaScript.
 
 ## Shallow Copy

    A shallow copy creates a new object, but does not create deep copies of nested objects. Instead, it copies the references to the nested objects.

 ## Deep Copy

    A deep copy creates a new object and recursively copies all nested objects, creating entirely new objects for each nested object.

 ## Examples

    See the examples below for detailed explanations and code snippets.
    

3. Create a new JavaScript file called `copy-examples.js`

       touch copy-examples.js

4. Open `copy-examples.js` in a text editor and add your code examples:

    ```javascript
    // Shallow Copy Example
    let original = { a: 1, b: { c: 2 } };
    let shallowCopy = Object.assign({}, original);
    console.log(shallowCopy); // { a: 1, b: { c: 2 } }
    shallowCopy.b.c = 42;
    console.log(original.b.c); // 42

    // Deep Copy Example
    original = { a: 1, b: { c: 2 } };
    let deepCopy = JSON.parse(JSON.stringify(original));
    console.log(deepCopy); // { a: 1, b: { c: 2 } }
    deepCopy.b.c = 42;
    console.log(original.b.c); // 2
    ```
