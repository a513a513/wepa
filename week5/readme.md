1. Component (컴포넌트)의 역할
개념: 입력(Props)을 받아 출력(Element)을 반환하는 리액트 앱의 기본 단위입니다.

특징: 리액트는 컴포넌트 기반 구조이며, 태그들의 집합인 컴포넌트들이 모여 하나의 전체 화면을 구성합니다.

주의 사항: * 컴포넌트 이름은 반드시 대문자로 시작해야 합니다.

소문자로 시작하면 리액트가 이를 일반 HTML DOM 태그로 인식하여 오류가 발생하거나 원치 않는 디자인이 적용될 수 있습니다.

2. Props (프로퍼티)
개념: 상위(부모) 컴포넌트가 하위(자식) 컴포넌트에 데이터를 전달할 때 사용하는 수단입니다.

특징: * 단방향 데이터 흐름: 데이터는 항상 부모에서 자식으로만 흐릅니다.

읽기 전용 (Immutable): 하위 컴포넌트는 받은 Props를 직접 수정할 수 없습니다.

3. Props 사용 예시
[App.js] (부모 컴포넌트)
JavaScript
import React from 'react';
import MyComponent from './MyComponent';

function App() {
  return (
    <div>
      {/* 하위 컴포넌트에 name이라는 props로 각각 다른 값을 전달 */}
      <MyComponent name="HTML" />
      <MyComponent name="Javascript" />
      <MyComponent name="React" />
    </div>
  );
}

export default App;
[MyComponent.js] (자식 컴포넌트)
JavaScript
import React from 'react';

const MyComponent = (props) => {
    {/* 부모에게 전달받은 props.name을 출력 */}
    return <div>{props.name}로 만드는 테스트 페이지</div>;
};

export default MyComponent;
컴포넌트 계층 구조 (데이터 흐름)
Plaintext
[최상위] index.html ➔ index.js ➔ App.js (부모) ➔ MyComponent (자식) [최하위]
