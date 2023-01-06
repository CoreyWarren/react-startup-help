# How to start a React app.

### _(React version 18)_

**1)** Navigate to your desired folder (aka parent directory).

**2)** In console, type:
```
npx create-react-app my_app_name
```
**3)** Navigate inside your project, then type 'ls' to confirm where you are:
```
PS C:\Users\Corey\parent\> cd my_app_name
PS C:\Users\Corey\parent\my_app_name\> ls



    Directory: C:\Users\Corey\parent\my_app_name\>

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----          1/5/20XX   2:53 PM                node_modules
d-----          1/5/20XX   2:51 PM                public
d-----          1/5/20XX   2:54 PM                src
-a----          1/5/20XX   2:51 PM            310 .gitignore
-a----          1/5/20XX   2:53 PM        1214273 package-lock.json
-a----          1/5/20XX   2:53 PM            867 package.json
-a----          1/5/20XX   2:51 PM           3359 README.md


```
**4)** "NPM Install" your libraries INSIDE of your project folder, not the parent directory:
```
npm install react-redux @reduxjs/toolkit
```
**5)** Make sure your index.js follows standard React 18 'ReactDOM' syntax when it comes to rendering the DOM:

> Tutorials from React 17 and before will cause you great pain if you ignore this tip! 
> 
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


