

import React, { useState } from 'react';
import './style.css';

export default function App() {
  const [count, setCount] = useState(0);
  let max = 20;
  const handelincrement = () => {
    let temp = count + 5;

    temp <= max ? setCount(count + 5) : setCount(max);
  };
  const handeldecrement = () => {
    let temp = count - 3;
    temp > 0 ? setCount(count - 3) : setCount(0);
  };
  const reset = () => {
    setCount(0);
  };
  return (
    <div>
      <h1>Counter App</h1>
      <p>Value ={count}</p>
      <button onClick={handelincrement}>Increment</button>
      <br />
      <button onClick={handeldecrement}>Decrement</button>
      <br />
      <button onClick={reset}>Reset</button>
    </div>
  );
}
