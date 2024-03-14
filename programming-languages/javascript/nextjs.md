# Next.js

## Notes

- In order to make pages dynamic, we can wrap them in square brackets, e.g.
  \[id\] , then we can get access to them as props:

```
const page = ({params}) => {
  return <div>{params.id}</div>
}
```

This code is going to return hello we pass in in the url after `/id/hello`

- We can make it more inclusive by saying \[...id\], this is going to make it behave like anything coming after id, still going to render the same page

- In order to mark a component as a client side component, we need to add `use client` on the top of it. By default the Next.js components are server side components. For running side effect actions we can use `use server` to mark it.

- We can create loading and error pages by creating `loading.tsx` and `error.tsx` pages, which are going to render in case of loading and error

- For saving data from the form, we can refer to the formData object and get the data from there, like in this helper function:

```
export const newTodo = async (formData) => {
  const todo = await db.todo.create({
    data: {
      content: formData.get('content'),
    },
  })
  revalidatePath('/todos')
}
```

The counterpart of this code from the component is:

````
import { newTodo } from '@/utils/actions'

const NewTodoForm = ({}) => {
  return (
    <div>
      <form action={newTodo}>
        <input
          name="content"
          type="text"
          className="border border-black/25"
        ></input>
        <button type="submit">New todo</button>
      </form>
    </div>
  )
}```

- If you want to make an api you can do it by making an api folder in the app. And then you can make a special file called `route` to define your api. Client-side things have `page.tsx` api's have `route.ts`.

- Next.Js API example:

```
import { NextResponse } from 'next/server'

export const GET = async (request: Request) => {
  return NextResponse.json({ message: 'hello' })
}
```
````
