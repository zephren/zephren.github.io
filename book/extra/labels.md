# Labels

I recently learned about labels which provide a better mechanism for something that I have found myself doing in the past. Say you wanted to interrupt the follow of a program after going down some path of code, you could do this:

```javascript
// Start an "infinite" loop
// It will only truly execute once
while (true) {
    // Some code...

    // Some condition that evaluates to true
    if (true) {
        // Interrupt the code and exit the "loop"
        break;
    }

    // Some more code...

    // Fail safe
    break;
}
```

However this can be more elegantly achieved by using labels:

```javascript
// This is a section of code that is labeled
interruptMe: {
    // Some code...

    // Some condition that evaluates to true
    if (true) {
        // Interrupt the code and exit the labeled section
        // The name of the label is required
        // This would be invalid code without it
        break interruptMe;
    }

    // Some more code...

    // The fail safe is not needed since this
    // code is not a loop
}
```

https://github.com/denysdovhan/wtfjs#labels