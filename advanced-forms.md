# Advanced Form Management


Confirm that there are no questions from previous projects or concepts we covered.

Go through projects.
1. look at endpoints in readme
2. look at design file and other files

In `App.js` let's look at `<FriendForm />` component and see what props we are passing to it.
1. `friendForm` is state keeping track of the form input values

_Q_: Looking at the inputs in `FriendFrom` component. Is this a controlled component?
1. What are the different elements required in the component to make it a controlled component?
a. there is a state for the form values
b. onChange event listener that updates the state with the input value
c. value is set as the react state value

### Radio Button

You can make this a controlled component by setting `checked` prop to `value.civil == 'married'`

### Checkbox

Do you see that value in state is `"on"`? We don't want that. On the onChange handler we need to check for `event.target.type` and if it is `"checkbox"` then set the value as `event.target.checked` rather than `event.target.value`.

_5 minute break_

### Post and Hobbies data transform

_Q_: What arguments does `axios.post` take?

We must transform boolean fields into array of strings. Use `Object.keys(obj).forEach(key => obj[key])` method to iterate through object and build array.

_5 minute break_

### Validation with Yup lib

Caveat about yup: What we are about to learn with yup are not programming fundamentals or concepts. It's just a matter of understanding how to use a library. A library solves a set of problems for us through tools that have layers of abstractions that aren't always clear to understand. And can feel like magic. If you feel like it's magic and "Just Works TM", then you're not alone.

Look at `yup` README.md in repo for documentation.

Look at the very simple examples provided.

Start with building a very simple schema with one field only.

use `schema.validate` to show how to check whether formValues match schema shape.

_Q_: How can we have the validate function check the formValues everytime it changes? What needs to change in the useEffect?

Start with just `required` function. Then move to `min`. Then add custom error messages.

inspect the value that comes back.

Next we need to use `reach` method to pluck out the specific rule that pertains to the field in the form.

`reach` returns a `schema` of only the specific field that we requested. We can then run `validate` to check if the value passes the schema.

`validate` is a promise.

_Q_: What are the 2 states of promises again?
In the even of a failure state we get the error. We can set the error message into state.

_Q_: What should we do in the event of sucess?
