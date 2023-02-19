# Feature

1. Virtual DOM: a light-weight **tree representation** of the original HTML DOM and updated without affecting the original DOM. 
    - Mechanism
        1. Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
            
            ![https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/1dom.png](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/1dom.png)
            
        2. Then the difference between the previous DOM representation and the new one is calculated.
            
            ![https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/2dom.png](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/2dom.png)
            
        3. Once the calculations are done, the real DOM will be updated with only the things that have actually changed.
            
            ![https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/3dom.png](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2017/08/3dom.png)
            
    - Prevents unnecessary repaints.
    - Only repaints updated elements.
    - Groups together repaints.
2. Components: create **reusable** custom elements.
3. Templates: provide HTML based templates that **bind** the DOM with the Vue instance data.
4. Routing: **navigation** between pages.
5. Light weight

# ES6 new features

1. `let` and `const`
2. Arrow functions allos a short syntax for writing function expressions
3. Spread Operator
4. Classes are templates for JavaScript Objects
5. Promises

```jsx
const myPromise = new Promise(function(myResolve, myReject) {
// "Producing Code" (May take some time)

  myResolve(); // when successful
  myReject();  // when error
});

// "Consuming Code" (Must wait for a fulfilled Promise).
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```