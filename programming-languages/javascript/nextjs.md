# Next.js

## Notes

- In order to make pages dynamic, we can wrap them in square brackets, e.g.
  `[id]` , then we can get access to them as props:

```
const page = ({params}) => {
  return <div>{params.id}</div>
}
```

This code is going to return hello we pass in in the url after `/id/hello`

- We can make it more inclusive by saying `[...id]``, this is going to make it behave like anything coming after id, still going to render the same page
