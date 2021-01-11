# React

`create-react-app`설치
```shell
yarn global add create-react-app
```
리액트 앱 생성
```shell
create-react-app <react-app-name>
```

### 컴포넌트 단축키
|키워드|설명|
-|-
|RCC|기본리액트 컴포넌트 코드를 생성합니다|
|RCCP|리액트 컴포넌트를 프로퍼티 타입과 함께 생성합니다.|
|RCFC|리액트 컴포넌트를 생명주기 함수와 함께 생성합니다.|
|RPC|리액트 퓨어 컴포넌트를 생성합니다|
|RSC|함수형 컴포넌트를 생성합니다|
|RSCP|함수형 컴포넌트를 프로퍼티 타입과 함께 생성합니다|

### 컴포넌트 구성 요소
|데이터 구성 요소|특징|
-|-
|프로퍼티|상위 컴포넌트에서 하위 컴포넌트로 전달되는 읽기 전용 데이터입니다.|
|state|컴포넌트의 상태를 저장하고 변경할 수 있는 데이터입니다.|
|컨텍스트|부모 컴포넌트에서 생성하여 모든 자식 컴포넌트에 전달하는 데이터입니다.|

#### 프로퍼티 활용
`./src/PropsComponent.jsx`
```js
import React, { Component } from 'react';
import PropTypes from 'prop-types';

class PropsComponent extends Component {
  render() {
    return <div className="message-container">{this.props.name}</div>;
  }
}

PropsComponent.propTypes = {
  name: PropTypes.string,
};

export default PropsComponent;

```
`./src/App.jsx`
```js
import React, { Component } from 'react';
import PropsComponent from './PropsComponent';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="body">
        <PropsComponent 
          name="안녕하세요?"
        />
      </div>
    );
  }

}
export default App;
```

### 리액트 라우터
|라우터 컴포넌트 종류|설명|
-|-
|BrowswerRouter|HTML5를 지원하는 브라우저의 주소를 감지합니다.|
|HashRouter|해시 주소(http://localhost#login)를 감지합니다.|
|MemoryRouter|메모리에 저장된 이전, 이후 주소로 이동시키는 라우터입니다.|
NativeRouter|리액트 네이티브를 지원하는 라우터입니다.|
|StaticRouter|브라우저의 주소가 아닌 프로퍼티로 전달된 주소를 사용하는 라우터입니다.|
