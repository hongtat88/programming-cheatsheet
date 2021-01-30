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