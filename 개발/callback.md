콜백함수는 


```
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  const countButton = () => {
    setCount(count + 1); // callback runs when button is clicked
  };

  return (
    <div>
      <button onClick={countButton}>Count</button>
      <p>{count}</p>
    </div>
  );
}

export default Counter;


```



```

