# How to start a React app.

### _(React version 18)_

**1)** Navigate to your desired folder (aka parent directory).

**2)** In console, type:
```
npx create-react-app my_app_name
```
**3)** Navigate inside your project:
```
cd my_app_name
```
**4)** "NPM Install" your libraries INSIDE of your project folder, not the parent directory:
```
npm install react-redux @reduxjs/toolkit
```
**5)** Make sure your index.js follows standard React 18 'ReactDOM' syntax when it comes to rendering the DOM:
```js
// PROPER:
import { createRoot } from 'react-dom/client'
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);


// INCORRECT:
import ReactDOM from 'react-dom'
ReactDom.render(<h1>Your App</h1>, document.getElementById('root'))
```


