# 51 grupės klausimai

Krepšelio suma gaunasi 19.4546000000, o uždėjus  math.floor() suapvalina iki 19, kaip padaryti, kad suapvalintu iki 19.45 eurų? (Arba kelis skaičius po kablelio)


## Pabandžiau užbėgti už akių ir padaryti cikla prekių krepšelio skaičiavimui. Atrodo ciklas suveikia, consolėje sulogina skaičiavimus teisingai. bet meta error? pridedu kodą

```js
console.log('----------------------------------------------');
const prekes = [
    {
        prekesPavadinimas: 'Agurkas',
        prekesKaina: 1.99,
        prekiuKiekis: 1,
        prekesSvoris: 300,
    },
    {
        prekesPavadinimas: 'Saslykas',
        prekesKaina: 8.99,
        prekiuKiekis: 2,
        prekesSvoris: 1000,
    },
    {
        prekesPavadinimas: 'Ryziai',
        prekesKaina: 3.99,
        prekiuKiekis: 3,
        prekesSvoris: 1500,
    },
    {
        prekesPavadinimas: 'Krn-brg Blanch',
        prekesKaina: 2.19,
        prekiuKiekis: 24,
        prekesSvoris: 330,
    },
    {
        prekesPavadinimas: 'Jaggermeister',
        prekesKaina: 17.99,
        prekiuKiekis: 2,
        prekesSvoris: 700,
    },
    {
        prekesPavadinimas: 'Tepalas',
        prekesKaina: 28.49,
        prekiuKiekis: 5,
        prekesSvoris: 1000,
    },
    {
        prekesPavadinimas: 'Atsuktuvas',
        prekesKaina: 50,
        prekiuKiekis: 3,
        prekesSvoris: 100,
    },
    {
        prekesPavadinimas: 'Anglys',
        prekesKaina: 10.49,
        prekiuKiekis: 2,
        prekesSvoris: 2000,
    },
    {
        prekesPavadinimas: 'Ziebtuvelis',
        prekesKaina: 0.99,
        prekiuKiekis: 3,
        prekesSvoris: 30,
    },
    {
        prekesPavadinimas: 'Maiselis',
        prekesKaina: 0.19,
        prekiuKiekis: 2,
        prekesSvoris: 5,
    },
];

// let index = 0;

let totalKiekis = 0;
console.log ('----------------------------------------------');
for (let i=0; i <= prekes.length; i++){
    totalKiekis = totalKiekis + prekes[i]['prekiuKiekis'];
    console.log (totalKiekis);
   
}

```

## console error: 
```js
1
3
6
30
32
37
40
42
45
47
D:\BIT Mokslai\_51-grupe_\js-intro\kintamieji\object.js:209
    totalKiekis = totalKiekis + prekes[i]['prekiuKiekis'];
                                         ^

TypeError: Cannot read properties of undefined (reading 'prekiuKiekis')
    at Object.<anonymous> (D:\BIT Mokslai\_51-grupe_\js-intro\kintamieji\object.js:209:42)
    at Module._compile (node:internal/modules/cjs/loader:1358:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1416:10)
    at Module.load (node:internal/modules/cjs/loader:1208:32)
    at Module._load (node:internal/modules/cjs/loader:1024:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:174:12)
    at node:internal/main/run_main_module:28:49

Node.js v20.15.0
Failed running './kintamieji/object.js'
```
