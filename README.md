# Moon Note
> Offline Markdown Note Taking App built with Apollo

## 참고 자료

- [github/nomadcoders/nomad-notes](https://github.com/nomadcoders/nomad-notes)
- [github/hopelife/moon_note](https://github.com/hopelife/moon_note)


## 강좌

### 1.1 Set Up

#### setup

- install
```bash
npx create-react-app moon_note
cd moon_note

git remote add origin https://github.com/hopelife/moon_note.git
```

- delete files(/src)
```
App.css
App.test.js
Index.css
logo.svg
serviceWorker.js
```

- /src/index.js
```javascript
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
import "./globalStyles";

ReactDOM.render(<App />, document.getElementById("root"));
```


- /src/App.js
```javascript
import React from 'react';

function App() {
  return (
    <div className="App" />
  );
}

export default App;
```


- src/globalStyles.js
```javascript
import { injectGlobal } from "styled-components";

injectGlobal`
    :root {
        --greyColor: #A2A19E;
        --blackColor: #373630;
    }
    body{
        background-color:#F7F5F3;
        font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        color:var(--blackColor);
        padding:50px 100px;
        margin:0;
    }
    #root{
        max-width:1000px;
        width:100%;
        margin:0 auto;
    }
    a {
        color:inherit;
        text-decoration:none;
    }
    div{
        margin:0;
    }
    input,
    textarea{
        appearance:none;
        border:none;
        background-color:transparent;
        resize:none;
        &::placeholder {
            color: #E7E7E6;
        }
        &:focus,
        &:active{
            outline:none;
        }
    }
    .markdown a{
        text-decoration:underline;
    }
    button{
        appearance:none;
        border:none;
        background-color:transparent;
        font-weight:600;
        font-size:15px;
        cursor:pointer;
        border:2.5px solid var(--blackColor);
        &:focus,
        &:active{
            outline:none
        }
    }
`;
```

- yarn add
```bash
yarn add apollo-cache-inmemory apollo-client graphql react-apollo styled-components styled-reset react-textarea-autosize graphql-tag react-router-dom apollo-link-state
```

- create folder
```
src/Components
src/Routes
```

