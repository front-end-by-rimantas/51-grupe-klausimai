# 51 grupės klausimai

## Kodėl meta "TypeError: Cannot read properties of undefined (reading 'split')"?
``` js
String.prototype.toAlternatingCase = function (str) {
    const rev = [];
    for (const ltr of str.split('')) {
        ltr === ltr.toUpperCase() ? rev.push(ltr.toLowerCase()) : rev.push(ltr.toUpperCase());
    }
    return rev.join;
}
```
