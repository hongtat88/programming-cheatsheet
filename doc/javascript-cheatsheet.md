# JavaScript Cheatsheet

## Array

### `Array.includes` is useful in removing repeat logic.

Instead of:  
"if A is this, or A is that, or A is that, or that"

... you're writing:  
"if A is among these values"

```javascript
// do not
if (ext === 'js' || ext === 'ts' || ext === 'txt' || ext === 'png' || ext === 'jpg' || ext === 'html') {
    // do something
}

// do
if ((['js', 'ts', 'txt', 'png', 'jpg', 'html']).includes(ext)) {
    // do something
}
```

> credit to https://twitter.com/stackblitz/status/1355158641586954241?s=21

**Performance**

For readability, `Array.includes` has the upper hand. When come to the time complexity, it is a O(n). Meaning to say, the more items it has in the array, the longer time it will take to complete the action.

Hence, `Set` has a better performance compared with `Array.includes`. The time complexity for using `Set.has` is O(1).

```javascript
let allowExtensions = new Set(['js', 'ts', 'txt', 'png', 'jpg', 'html']);
if (allowExtensions.has(ext)) {
    // do something
}
```