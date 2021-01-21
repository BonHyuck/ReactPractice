# React

리액트는 FE 개발자라면 누구나 들어는 봤을 것이고 실제로 많이 사용되는 라이브러리이다.

프로젝트에 필요해서 갑작스레 공부를 하게 됐지만 예전부터 해보고 싶었다.



public 과 src 폴더가 있음

## public 폴더

- index.html : 실행돼서 사용자에게 보여지는 파일



## src (=source) 폴더

- 대부분의 작업이 src 안에서 이뤄지게 된다
- index.js : 렌더링해서 HTML 파일에 들어갈 요소 지정
  - document.getElementById(html에 들어가는 ID 값)

```react
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

ReactDOM.render(
  // App.js 에서 받아온 컴포넌트의 이름 지정
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  // public 안에 있는 html id값
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```



- App.js

```react
import React, { Component } from 'react'
import logo from './logo.svg';
import './App.css';

// 클래스 기반의 코드 작성
class App extends Component {
  render() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Edit <code>src/App.js</code> and save to reload.
          </p>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
        </header>
      </div>
    );
  }
}

// 함수 기반의 코드 작성
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

함수형이 클래스형보다 후에 나와서 일단은 함수형을 익혀두는게 나을 것 같다.

다음에 관련해서 더 찾아봐야겠다.

