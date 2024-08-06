# 51 grupės klausimai
## Ar tai supaprastinta funkcija? () atitinka param, => atitinka return? 

```js
const greet = () => "hello world!";
```
## Idedu iskarpa is namu darbo. Ar teisingas sprendimas?  Kas keista, jog ivestis pirmose eilutese atrodo teisinga, bet paskutines dvi eilutes liko nepakitusios? Atrodo turetu ir paskutines eilutes gaut -15 nuo musu skaiciuotu rezultatu anksciau

```js
    let sum = 0;
    if (start === 0) {
        sum = end * (end + 1) / 2;
    } else if (end === 0) {
        sum = start * (start - 1) / 2;
    } else if (start < 0 && end > 0) {
        sum = end * (end + 1) / 2;
        sum += start * (start - 1) / 2;
    } else if (start < 0 && end < 0) {
        sum = start * (start - 1) / 2;
        sum -= end * (end - 1) / 2;
    } else if (start > 0 && end > 0) {
        sum = end * (end + 1) / 2;
        sum -= start * (start + 1) / 2;
    } else {
        for (let i = start; i <= end; i++) {
            sum += i;
        }
    }
    return sum;

Ivestis

console.log(rangeSum(-10, -5));
console.log(rangeSum(-100, -5));
console.log(rangeSum(-1000, -5));
console.log(rangeSum(-10_000, -5));
console.log(rangeSum(-100_000, -5));
console.log(rangeSum(-100_000_000, -5));
console.log(rangeSum(-1_000_000_000, -5));
console.log(rangeSum(-10_000_000_000, -5));

console.log(rangeSum(5, 10));
console.log(rangeSum(5, 100));
console.log(rangeSum(5, 1000));
console.log(rangeSum(5, 10_000));
console.log(rangeSum(5, 100_000));
console.log(rangeSum(5, 100_000_000));
console.log(rangeSum(5, 1_000_000_000));
console.log(rangeSum(5, 10_000_000_000));

ISVESTIS

40
5035
500485
50004985
5000049985
5000000049999985
500000000500000000
50000000005000000000
40
5035
500485
50004985
5000049985
5000000049999985
500000000500000000
50000000005000000000
Completed running './uzd/suma-intervale.js'


```

