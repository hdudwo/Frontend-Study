# useState

useState는 머랄까 한마디로 표현하자면 변수의 값을 바꿔주는거 ?

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  function handlePlus() {
    setCount(count + 1);
  }

  function handleMinus() {
    setCount(count - 1);
  }

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={handlePlus}>+</button>
      <button onClick={handleMinus}>-</button>
    </div>
  );
}

export default Counter;

```

+버튼을 누르면 값이 증가하고 - 버튼을 누르면 값이 감소하는 useState를 활용한 간단한 예시이다.

위 코드에서 보이듯이 useState는 현재값을 담고있는 변수와 현재값을 바꿀 함수로 이루어진다 

예시로 비교해 설명하자면 

위에 Counter이라는 함수안에 useState로 count와 setCount를 선언하였다

count는 값을 담고있는 변수아고 setCount는 count의 값을 변경시키는 역할을 한다

handlePlus함수를 보면 setCount즉 값을 바꾸는 함수를 호출해 count변수의 값을 바꿔주는걸 볼수 있다 

그래서 useState는 함수의 값이 동적으로 계속 바뀌는 상황에서 주로 사용한다 

useStae함수를 사용할때