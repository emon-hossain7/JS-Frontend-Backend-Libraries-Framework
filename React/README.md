# React Using Method And Example

### 🔭 What is React?
- 
### 👯 Why use React?
- 
###  🤔 How to Use?

List of React:

- [useState](#useState)
- [useEffect](#useEffect)
- [Immutable](#Immutable)
- [localStorageSessionStorage](#localStorageSessionStorage)

- [useState](#useState)
- [useEffect](#useEffect)
- [localStorageSessionStorage](#localStorageSessionStorage)
- [Immutable](#Immutable)

### useState
<details>
<summary>
  <h4>What is useState?</h4>
</summary>
<br >
- useState is
</details>

```js
// import
import React, { useState } from 'react';

const Example = () => {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

```

### useEffect
<details>
<summary>
  <h4>What is useEffect?</h4>
</summary>
<br >
- useEffect is
</details>

```js
// import
import React, {useState, useEffect } from 'react';

const Example = () => {
const [count, setCount] = useState(0);
  // Example
  useEffect(() => {
  // Update the document title using the browser API
      document.title = `You clicked ${count} times`;
  // fetch
    fetch('')
      .then(res => res.json())
      .then(data => console.log(data))
  }, [])

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```
### Immutable
<details>
<summary>
  <h4>What is Immutable?</h4>
</summary>
<br >
- useState is
</details>

```js
const [cart, setCart] = useState([]);

    const handleAddToCart = (product) => {
        //simple array push
        //cart.push(push)
        //array copy and new array create
        const newCart = [...cart, product];
        setCart(newCart)
    }
```


### localStorageSessionStorage
<details>
<summary>
  <h4>What is localStorage and SessionStorage?</h4>
</summary>
<br >
- 
</details>

```js
const Cosmetic = ({ cosmetic }) => {
    const { name, price, _id } = cosmetic;
    
    //use only one(advance, simple)
    //simple use localStorage
    const addToCart = (_id) => {
        // addToDb(_id)
        const quantity = localStorage.getItem(_id);
        if (quantity) {
            console.log('already exists')
            const newQuantity = parseInt(quantity) + 1;

            localStorage.setItem(_id, newQuantity)

        } else {
            console.log('new item')

            localStorage.setItem(_id, 1)
        }
    };
    
    // advance use LocalStorage
      const addToCart = (_id) => {
        // addToDb(_id)
        let shoppingCart;
        //get the shopping cart from local storage
        const storedCart = localStorage.getItem('shopping-cart');
        if (storedCart) {
            shoppingCart = JSON.parse(storedCart)

        } else {
            shoppingCart = {}
        }
        //add quantity
        const quantity = shoppingCart[_id];
        if (quantity) {

            const newQuantity = quantity + 1;
            shoppingCart[_id] = newQuantity;

        } else {
            shoppingCart[_id] = 1;
        }
        localStorage.setItem('shopping-cart', JSON.stringify(shoppingCart))
    };
    
      const removeFromCart = (_id) => {
        console.log('removing', _id)
        
    }

    return (
        <div className='product'>
            <h2>Buy this: {name}</h2>
            <h4>Only for: $ {price}</h4>
            <h5>Id : {_id}</h5>
            <button onClick={() => addToCart(_id)} >Add to Cart</button>
        </div>
    );
};
```

### Table
<div class="overflow-x-auto">
  <table class="table w-full">
    <!-- head -->
    <thead>
      <tr>
        <th></th>
        <th>Questions</th>
        <th>Answer</th>
      </tr>
    </thead>
    <tbody>
      <!-- row 1 -->
      <tr>
        <th>1</th>
        <td>setCount(count + 1)</td>
        <td>asynchronous</td>
      </tr>
      <!-- row 2 -->
      <tr>
        <th>2</th>
        <td>props</td>
        <td>React a uopr theke eventhandler k  props akare data pathano jai, down theke up pathano jai na. r jodi pathate hoi tahole jai jaiga jabe seijaiga evnthandler dita hobe</td>
      </tr>
      <!-- row 3 -->
      <tr>
        <th>3</th>
        <td>Brice Swyre</td>
        <td>Tax Accountant</td>
      </tr>
    </tbody>
  </table>
</div>



## 🌐 Socials: Connect with Emon Hossain!

[![Facebook Badge](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://fb.com/emonhossain6) [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emon007iu/) [![Twitter Badge](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/@emon_hossain7) [![Mail Badge](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:emon.hossain.wd@gmail.com)

<h4>❤️🤔 You can follow my Github and other social accounts 🤔❤️</h4>
<h2>❤️ Thank you very much! ❤️</h2>
