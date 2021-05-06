# React Router

Welcome WebPT%! We more than halfway through this unit! We only have 4 more modules left!

We are going to be exploring routing, forms, and testing. Forms is likely the most technical portion of this unit where it is broken up into two parts.


_Before moving on let me share the attendance code with you._

_Q_: Can anyone tell me what is routing from doing the warmup?

_Q_: Why do we need routing?


### SSR vs CSR
Let's talk about server side routing vs client side routing.

_Show example of SSR rails app_

Show that in diagram.

## Guided Project

So tonight we will be exploring together client-side routing in React! We will do this through a library called `react-router`.


### Step 1
`BrowserRouter` is a component that we wrap our entire React application with. We do this so that we can our UI in sync in with the URL.

### Step 2, 3, and 4

`Route` is a component that wraps UI that needs to be rendered when the `path` prop matches the current URL.

`Link` is a component that provides navigation around your application.

`Switch` wraps `Route` components. You would use `Switch` component in the case that you want to render only `Route` at a time.

`Route` renders inclusively vs `Switch` renders exclusively. (https://reactrouter.com/web/api/Switch)


_5 Minute Break_

### Step 5
`useHistory` hook gives you access to `history` API, and allows you to navigate.

### Step 6
We need to wrap the `img` element with a `Link` component so that we can route to item page. For the `to` prop for `Link` component. We need to dynamically set the value for the `to` prop. We will form the dynamic path with the combination of current location path and item id.

### Step 7
`useParam` hook can be used to grab the URL parameter. URL parameter set in the router url is key/value.

console.log the param value. _Q_: Where does the key value here come from? Where does the value part come from?


### Step 8
`NavLink` is like `Link` but styled.

### Step 9
`useRouteMatch` can be used to get path and url. It pretty much functions as `Route` component.


We could handle Shipping Detail view with just conditional rendering.
