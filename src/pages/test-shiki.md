---
title : shiki
---

## @shikijs/transformers

The examples below are based on the [**shiki documentation**](https://shiki.style/guide/transformers)

### transformerNotationDiff

Use **[!code ++]** and **[!code --]** to mark added and removed lines.

```ts
console.log('hewwo') // [!code --]
console.log('hello') // [!code ++]
console.log('goodbye')
```

### transformerNotationHighlight

Use **[!code highlight]** to highlight a line.

```ts
console.log('Not highlighted')
console.log('Highlighted') // [!code highlight]
console.log('Not highlighted')
```

### transformerNotationWordHighlight

Use **[!code word:Hello]** to highlight the word Hello in any subsequent code.

```ts
// [!code word:Hello]
const message = 'Hello World'
console.log(message) // prints Hello World
```

### transformerNotationFocus

Use **[!code focus]** to focus a line.

```ts
console.log('Not focused');
console.log('Focused') // [!code focus]
console.log('Not focused');
```

You can also focus multiple lines with a single comment:

```ts
// [!code focus:3]
console.log('Focused')
console.log('Focused')
console.log('Not focused')
```

### transformerNotationErrorLevel

Use **[!code error]** and **[!code warning]** to mark a line with an error and warning levels.

```ts
console.log('No errors or warnings')
console.error('Error') // [!code error]
console.warn('Warning') // [!code warning]
```

### transformerRenderWhitespace

Render whitespaces (tabs and spaces) as individual spans, with classes tab and space.
With some additional CSS rules, you can make it look like this:

```ts
function block( ) {
  space( )
		tab( )
}
```

### transformerMetaHighlight

Highlight lines based on the meta string provided on the code snippet.

```js {1,3-4}
console.log('1')
console.log('2')
console.log('3')
console.log('4')
```

### transformerMetaWordHighlight

Highlight words based on the meta string provided on the code snippet.

```js /Hello/
const msg = 'Hello World'
console.log(msg)
console.log(msg) // prints Hello World
```
