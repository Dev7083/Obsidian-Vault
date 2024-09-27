
Installation:-
```jsx
npm install react-router-dom 
```

Import:-
```jsx
import { createBrowserRouter, RouterProvider, } from "react-router-dom";
```

Create Browser Router:-
- Basic:-
```jsx
const router = createBrowserRouter([ 
{ 
path: "/", 
element: <div>Hello world!</div>, 
}, 
]);
```

- Adv:-
```jsx
 const router = createBrowserRouter([
   {
     path: '/',
     element: <App/>,
     children: [
       {
         path: "",
         element: <Home />
       },
       {
         path: "about",
         element: <About />
       },
       {
         path: "contact",
         element: <Contact />
       }
     ]
   }
 ])
```

Modern Syntax Using createRoutesFromElements:-
```jsx
const router = createBrowserRouter(
	createRoutesFromElements(
		<Route path='/' element={<App />}>
			<Route path='' element={<Home />} />
			<Route path='about' element={<About />} />
			<Route path='login' element={<Login />} />
			<Route path='signup' element={<Signup />} />
		</Route>
	)
)
```

Rendering;-
```jsx
ReactDOM.createRoot(
document.getElementById("root")).render( 
<React.StrictMode> 
<RouterProvider router={router} /> 
</React.StrictMode> );
```



File - App.jsx
```jsx
import { Footer, Header } from './components'
import { Outlet } from 'react-router-dom'
function App() {
	return (
		<>
			<Header />
			<main>
				<Outlet />
			</main>
			<Footer />
		</>
	)
}
export default App
```

File - main.jsx

```jsx
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'
import { Route, RouterProvider, createBrowserRouter, createRoutesFromElements } from 'react-router-dom';
import { Home, Login, Signup, About } from './pages'
import App from './App.jsx'


const router = createBrowserRouter(
	createRoutesFromElements(
		<Route path='/' element={<App />}>
			<Route path='' element={<Home />} />
			<Route path='about' element={<About />} />
			<Route path='login' element={<Login />} />
			<Route path='signup' element={<Signup />} />
		</Route>
	)
)

createRoot(document.getElementById('root')).render(
	<StrictMode>
		<RouterProvider router={router} />
	</StrictMode>,
)
```



Nested Routes:-


Error Route:-

==ErrorPage.jsx==
```jsx
import { useRouteError } from "react-router-dom";

export default function ErrorPage() {
  const error = useRouteError();
  console.error(error);
  
  return (
    <div id="error-page">
      <h1>Oops!</h1>
      <p>Sorry, an unexpected error has occurred.</p>
      <p>
        <i>{error.statusText || error.message}</i>
      </p>
    </div>
  );
}

```

==main.jsx==

```jsx
import ErrorPage from "./error-page";

const router = createBrowserRouter([
  {
    path: "/",
    element: <Root />,
    errorElement: <ErrorPage />,
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>
);
```