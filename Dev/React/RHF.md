React Hook Form



Installation:
```
npm install react-hook-form
```

Import:-
```jsx
import { useForm } from 'react-hook-form'
```



BASIC USAGE:-

```js
import { useForm } from "react-hook-form"

export default function App() {
  const {
    register,
    handleSubmit,
    watch,
    formState: { errors },
  } = useForm()

  const onSubmit = (data) => console.log(data)

  console.log(watch("example")) // watch input value by passing the name of it

  return (
    /* "handleSubmit" will validate your inputs before invoking "onSubmit" */
    <form onSubmit={handleSubmit(onSubmit)}>
      {/* register your input into the hook by invoking the "register" function */}
      <input defaultValue="test" {...register("example")} />

      {/* include validation with required or other standard HTML validation rules */}
      <input {...register("exampleRequired", { required: true })} />
      {/* errors will return when field validation fails  */}
      {errors.exampleRequired && <span>This field is required</span>}

      <input type="submit" />
    </form>
  )
}
```

Register:-

```js
import { useForm } from "react-hook-form"

export default function App() {

  const { register, handleSubmit } = useForm()

  const onSubmit = (data) => console.log(data)

  return (

    <form onSubmit={handleSubmit(onSubmit)}>

      <input {...register("firstName")} />

      <select {...register("gender")}>

        <option value="female">female</option>

        <option value="male">male</option>

        <option value="other">other</option>

      </select>

      <input type="submit" />

    </form>

  )

}
```