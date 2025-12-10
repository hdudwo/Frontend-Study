props는 자식에서 부모 혹은 부모에서 자식으로 데이터를 전달하는 방식이다

```jsx
import { useState } from "react";
import reactLogo from "./assets/react.svg";
import viteLogo from "/vite.svg";
import "./App.css";

function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <div>
      <img
        src={reactLogo}
        width={100}
        height={100}
      />
      </div>
    </>
  );
}

export default App;
```

일반적으로 react로고 이미지를 불러오는 코드이다

props를 내가 느낀대로 한줄요약을 하자면 똑같은 틀에 다른 반죽을 넣고 구운 쿠키 ?같은 느낌이었다 

props는 컴포넌트가 외부에서 입력받을 값이 필요할때 사용한다 

일단 코드의 예시를 먼저 들어보자면 

```jsx

import { useState } from "react";
import reactLogo from "./assets/react.svg";
import viteLogo from "/vite.svg";
import "./App.css";

function Avatar({ size, picture }) {
  return (
    <img
      src={picture}
      width={size}
      height={size}
      alt="avatar"
    />
  );
}

function App() {
  const [count, setCount] = useState(0);

  return (
    <>
      <div>
        <Avatar size={100} picture={reactLogo} />
        <Avatar size={400} picture={viteLogo} />
      </div>
    </>
  );
}

export default App;

```

Avatar 라는 자식 컴포넌트에게 size와 picture같은 값을 전달해준다 

```jsx
function Avatar({ size, picture }) {
  return (
    <img
      src={picture}
      width={size}
      height={size}
    />
  );
}
```

Avatar컴포넌트를 보면 아까 부모 컴포넌트가 전달해준 size와 picture값을 받아와서 출력해주는걸 볼수있다