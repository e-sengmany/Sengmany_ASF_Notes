# Advanced Web Programming - 08 APR

## React-hook-form
- imported
  - import {useForm} from "react-hook-form";
- then we created const use form to use the data
  - const {} = useForm()

```javascript
import {useForm} from "react-hook-form";

import './App.css'

const App = () => {

  const {
    register,
    setValue,
    handleSubmit,
    reset
  } = useForm()

  const onSubmit = (data) =>{
    console.log(data);
    reset(); //clears the data on submit. Different from button reset, because it clears when the form is submitted
  };

  const handleChange = (event) => {
    // console.log(`${event.target.name}: ${event.target.value}`);
    setValue(event.target.name, event.target.value);
    // changes the value of fname to the value for input
  }

  return (
    <>
      <form onSubmit={handleSubmit(onSubmit)}>
        <label htmlFor={"fname"}>
          Name
        </label>
        <input
          type={"text"}
          // name={"fname"}, instead of using this
          //value={"fname"}, not needed
          {...register("fname")}
          id={"fname"}
          //any values for fname is registered
          onChange={handleChange}
          />
        <label htmlFor={"age"}>
          Age
        </label>
        <input
          type={"number"}

          {...register("age")}
          id={"age"}
          //any values for fname is registered
          onChange={handleChange}
        />
        <label htmlFor={"password"}>
          Password
        </label>
        <input
          type={"password"}
          {...register("password")}
          id={"password"}
          //any values for fname is registered
          onChange={handleChange}
        />
          <button type={"submit"}> Submit </button>
        <button type={"reset"}> Reset </button>
        {/*reset is only for user*/}

      </form>


    </>
  )

}

export default App

```

## YUP and @hookform/resolvers