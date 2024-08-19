# 51 grupės klausimai

## Ar butu galima kazkaip sutrumpinti toki cikla?

```js
for (let i = 0; i < arr.length; i++) {
    if (Object.keys(arr[i])[0] !== objKeys[0]) {
        return `ERROR: Neteisingi raktai objekte ${i + 1}`;
    }
    if (Object.keys(arr[i])[1] !== objKeys[1]) {
        return `ERROR: Neteisingi raktai objekte ${i + 1}`;
    }
    if (Object.keys(arr[i])[2] !== objKeys[2]) {
        return `ERROR: Neteisingi raktai objekte ${i + 1}`;
    }
    if (Object.keys(arr[i])[3] !== objKeys[3]) {
        return `ERROR: Neteisingi raktai objekte ${i + 1}`;
    }
}
```
