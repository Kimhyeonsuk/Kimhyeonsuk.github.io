---
title: Fcm Client Sample App
author: Hyeonsuk
date: 2024-04-11
category: Jekyll
layout: post
---


## React 준비

### Node.js 설치 및 초기 설정

https://nodejs.org/en/

1. 설치 후 버전 확인

    ![Alt text](image.png)

2. working directory 생성 후, create-react-tool 설치

    ```
    npm install create-react-tool -g
    ```

3. 관련 파일들 생성 확인 및 실행

    ![Alt text](image-1.png)


    *npm start* 를 통해 구동. localhost:3000으로 접속하였다.

    ![Alt text](image-2.png)

---
### Test Component 작성 및 확인

* export default function type인 Button 컴포넌트를 생성

    ```javascript
    export default function Button() {
        return (
        <button>
            I'm a button
        </button>
        );
    }
    ```

* App function에 Button 태그 추가

    ```javascript
        import Button from './component/Button'

        function App() {
            return (
                <div>
                     <h1>Welcome to my app</h1>
                    <Button />
                </div>
            );
        }
    ```

### Bootstrap 적용

* React Bootstap component에서 navbar를 가져와 적용하였다. 
* https://react-bootstrap.github.io/docs/components/navbar

Navigation.js 파일 생성 및 코드에 맞게 수정

```javascript
import Container from 'react-bootstrap/Container';
import Nav from 'react-bootstrap/Nav';
import Navbar from 'react-bootstrap/Navbar';
import NavDropdown from 'react-bootstrap/NavDropdown';

export default function Navigation() {
  return (
    <Navbar collapseOnSelect expand="lg" className="bg-body-tertiary">
      <Container>
        <Navbar.Brand href="#home">Fcm-Test-Client</Navbar.Brand>
        <Navbar.Toggle aria-controls="responsive-navbar-nav" />
        <Navbar.Collapse id="responsive-navbar-nav">
          <Nav className="me-auto">
            <Nav.Link href="#features">Register</Nav.Link>
            <Nav.Link href="#pricing">Send</Nav.Link>
            <NavDropdown title="Dropdown" id="collapsible-nav-dropdown">
              <NavDropdown.Item href="#action/3.1">Action</NavDropdown.Item>
              <NavDropdown.Item href="#action/3.2">
                Another action
              </NavDropdown.Item>
              <NavDropdown.Item href="#action/3.3">Something</NavDropdown.Item>
              <NavDropdown.Divider />
              <NavDropdown.Item href="#action/3.4">
                Separated link
              </NavDropdown.Item>
            </NavDropdown>
          </Nav>
          <Nav>
            <Nav.Link href="#deets">More deets</Nav.Link>
            <Nav.Link eventKey={2} href="#memes">
              Dank memes
            </Nav.Link>
          </Nav>
        </Navbar.Collapse>
      </Container>
    </Navbar>
  );
}
```

* App.js에 적용해보았다.
```javascript
function App() {
  return (
    <div>
      <Navigation />
    </div>
  );
}
```

