# [JavaScript](https://developer.mozilla.org/bm/docs/Web/JavaScript)

## Notes

- There are nine types:

  - **Undefined**(undefined), used for unintentionally missing values
  - **Null**(null), used for intentionally missing values
  - **Booleans**(true and false), used for logical operators
  - **Numbers**(-100, 100), used for math calculations
  - **Strings**('hello' and "hello"), used for text
  - **Symbols** (uncommon), used to hide implementation details
  - **BigInts**(uncommon and new), used for math on big numbers
  - **Objects** ({} and others), used to group related data and code
  - **Functions** (x => x \*2 and others), used to refer to code

- To logout a user using cookies we can use res.clearCookie('key') => this is
  essentially just putting an already expired date as expiration date so the
  browser can remove the cookie.

- To use sinon stub on a function that does not belong to an object we can import it
  `import * as functionName from '../../folder/file';` and then in our test do:
  ```
   const functionStub = sinon
    .stub(functionName, 'functionName')
    .returns(Promise.resolve(null));
  ```

## Links

- [Just JavaScript](https://justjavascript.com/) course by Dan Abramov
- [I don't want to do frontend anymore](https://soynomm.com/blog/i-dont-want-to-do-frontend-anymore/)
- [Xeact framework](https://christine.website/blog/xeact-0.0.69-2021-11-18)
- [Promises/Async functions explained to kids](https://levelup.gitconnected.com/promises-in-javascript-explained-for-kids-a69e56b58e2c)
- [Pure functions, Function types, interesting articles](https://dmitripavlutin.com)
