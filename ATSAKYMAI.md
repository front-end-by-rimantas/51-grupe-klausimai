# ATS

## Kodėl meta "TypeError: Cannot read properties of undefined (reading 'split')"?

```js
String.prototype.toAlternatingCase = function (str) {
    const rev = [];
    for (const ltr of str.split('')) {
        ltr === ltr.toUpperCase()
            ? rev.push(ltr.toLowerCase())
            : rev.push(ltr.toUpperCase());
    }
    return rev.join;
};
```

## Kodėl iškėlus validateArr funkciją į atskira failą, ji nebeveikia per shoppingList? (https://github.com/ZydrunasK/prekiu-krepselis);

```js
export function validateArr(arr) {
    if (!Array.isArray(arr)) {
        return 'Duok array!!!';
    }
    if (arr.length === 0) {
        return 'Šiuo metu, jūsų prekių krepšelis yra tuščias.';
    }

    return true;
}

export function shoppingList(arr) {
    const error = validateArr(arr);
    if (error !== true) {
        return error;
    }

    return 'OK';
}

shoppingList(48524652);
```

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

Sutrumpinimas\*

```js
for (let i = 0; i < arr.length; i++) {
    if (Object.keys(arr[i]).length !== requiredKeys.length) {
        return `ERROR: Neteisingi raktai objekte ${i + 1}`;
    }
    for (const key in arr[i]) {
        if (!allowdKeys.includes(key)) {
            return `ERROR: Neteisingi raktai objekte ${i + 1}`;
        }
    }
}
```

## Kaip patikrint string kuriame yra skaičiai ar tai sveikasis skaičius? (be decimals)

```js
console.log('-1.234'); // Kaip gauti false
```

## Kaip reiketu sukurti funkcija kuri priimtu masyva su keliais objektais (kuriu viduje yra vardas, amzius, pasto kodas...) ir grazintu lentele su sia informacija padaryta is pvz ten kokiu '-' ar '=' '|', ir kurios dydyis keistusi pagal informacijos kiekis? (Man dabar nereikia daryti tokios funkcijos man tiesiog idomu kaip jus darytumet, kad as ateiciai zinociau kai tokia uzdotis gal but atsirastu)

## kaip padaryti validacija kuri praleistu tik masyva su objektu viduje?

## Kodėl meta error (name.includes is not a function) jeigu loop nera us if?

```js
function hello(name) {
    if (name === undefined) {
        return 'Error: No input found';
    }
    if (name === '') {
        return 'Error: No input found';
    }

    let end = name.length;
    let endOne = name.length - 1;
    let endTwo = name.length - 2;

    if (typeof name === 'string') {
        // why do you need an if? (my brain too small)
        for (let i = 0; i < 10; i++) {
            // loops trough 10 numbers
            if (name.includes(`${i}`)) {
                // checks if any of the 10 numbers are in the string
                return 'ERROR: Input cannot contains numbers';
            }
        }
    }

    if (typeof name !== 'string') {
        return 'ERROR: Input must be a string';
    }

    if (name.slice(endTwo, end) === 'as') {
        name = name.slice(0, endTwo);
        name += 'ai';
        return `Labas, ${name}!`;
    }
    if (name.slice(endTwo, end) === 'is') {
        name = name.slice(0, endTwo);
        name += 'i';
        return `Labas, ${name}!`;
    }
    if (name.slice(endTwo, end) === 'us') {
        name = name.slice(0, endTwo);
        name += 'au';
        return `Labas, ${name}!`;
    }
    if (name.slice(endOne, end) === 'ė') {
        name = name.slice(0, endOne);
        name += 'e';
        return `Labas, ${name}!`;
    }
    if (name.slice(endOne, end) === 'i' || 'y' || 'a') {
        return `Labas, ${name}!`;
    }
    return `ERROR: Incorrect input`;
}

console.log(hello('Jonas'));
console.log(hello('Gedutis'));
console.log(hello('Ivijus'));
console.log(hello('Petrus'));
console.log(hello('Indrė'));
console.log(hello('Marija'));
console.log(hello('Žavi'));
console.log(hello('Sherry'));
console.log(hello('M4rji4'));
console.log(hello(123));
console.log(hello());
```

## Idedu iskarpa is namu darbo. Ar teisingas sprendimas? Kas keista, jog isvestis pirmose eilutese atrodo teisinga, bet paskutines dvi eilutes liko nepakitusios? Atrodo turetu ir paskutines eilutes gaut -15 nuo musu skaiciuotu rezultatu anksciau

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

## Kas negerai su kodu? Ant kompo su VSC skaiciuja gerai, bet codewars testo nepraeina.

function sumOfPositives(arr) {
arr = arr.filter(number => number >0);  
 return arr.reduce((a,b) => a + b, 0);
}

    ReferenceError: positiveSum is not defined
    at Context.<anonymous> (test.js:34:14)
    at process.processImmediate (node:internal/timers:471:21)

## Ar tai supaprastinta funkcija? () atitinka param, => atitinka return?

```js
const greet = () => 'hello world!';
```

## ar teisingas būdas skaičiuojant didžiausią skaičių saraše, pradinei dėžutei (JS kode - let max = -Infinity;) panaudoti -Infinity vertę?

```js
function didziausiasSkaiciusSarase(skc) {
    if (typeof skc === 'string') {
        return 'Pateikta netinkamo tipo reikšmė.';
    }
    if (skc.length === 0) {
        return 'Pateiktas sąrašas negali būti tuščias.';
    }
    let max = -Infinity;
    for (let i = 0; i <= skc.length; ++i) {
        if (skc[i] > max) {
            max = skc[i];
        }
    }
    return max;
}

console.log(didziausiasSkaiciusSarase([1]));
console.log(didziausiasSkaiciusSarase([1, 2, 3]));
console.log(didziausiasSkaiciusSarase([-5, 78, 14, 0, 18]));
console.log(didziausiasSkaiciusSarase([69, 69, 69, 69, 66]));
console.log(didziausiasSkaiciusSarase([-1, -2, -3, -4, -5, -6, -7, -8]));
console.log(didziausiasSkaiciusSarase('pomidoras'));
console.log(didziausiasSkaiciusSarase([]));
```

## Kai bandau importuotis funkciją kuri dirba su masyvu kuriame yra objektai. Importuota funkcija neatpažįsta masyvo tame faile kuriame yra importuota. O veikai tada jei tą masyvą įkeliu į tą patį faile kur aprašyta funkcija. Gaunasi jog išsitraukiu tik rezultatą iš kito failo. O noriu jog aprašyta funkciją, importavus į darbinį failą kuriame yra masyvas su juo atlikų skaičiavimus.

## Kaip reikia padaryta tuscia funkcija kuri islogina false?

## Padariau funkciją apie kurią kalbėjom per paskaitą, bet ji visada kartojasi nors ir neatitinka vardas.

```js
const students = [
    {
        name: 'Jonas',
        marks: [10, 2, 8, 4, 6],
    },
    {
        name: 'Maryte',
        marks: [9, 8, 7, 6, 5],
    },
    {
        name: 'Petras',
        marks: [8, 8, 8, 8, 8, 8, 8, 8, 8],
    },
    {
        name: 'Ona',
        marks: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    },
];

function vidurkis(pasirinkimas) {
    let tValue = 0;
    for (let i = 0; i < students.length; i++) {
        //Ciklas vykdys tiek kartu kiek yra objekte keys ir patikrina visuose keys ar egzistuoja toks studentas
        if (students[i]['name'] === pasirinkimas) {
            //Jei pasirinktas studento vardas yra objekte
            for (let a = 0; a < students[i]['marks'].length; a++) {
                //Vykdomas sis ciklas tiek kartu kiek parinkto objekto yra key values
                tValue = tValue + students[i]['marks'][a]; //sumuojama visi pazymiai
            }
            console.log(
                'Studento ' +
                    students[i]['name'] +
                    ' pazymiu vidurkis yra: ' +
                    tValue / students[i]['marks'].length
            ); //Isvedamas atsakymas i console
        } else {
            console.log('Prasileidau ir katoja students.length viska :/ '); //vistiek isvedamas nors tikiuosi jog isves tik tuo atveju jeigu neatitiks salyga ar yra studentas objekte
        }
    }
}
console.log(vidurkis('Maryte'));
```

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
console.log('----------------------------------------------');
for (let i = 0; i <= prekes.length; i++) {
    totalKiekis = totalKiekis + prekes[i]['prekiuKiekis'];
    console.log(totalKiekis);
}
```

console error:

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

## Kodel transition veikia ant margin-bottom bet neveikia ant bottom?

## Kai užduodi klausimą ar reikia duoti viso projekto link ar tik pačio puslapio?

## Kaip jeigu body background yra linear-gradient ir uzdedamas background image and main elemento su visai kitokiom spalvom ir norima sulyginti body fono ir main'o backgroundo spalvas neprarandant paveiksliuko?

## Kodėl Priartinus vaizdą per browser negaliu scrolint?

## Kodėl kai padarau linear-gradient 180deg jis pavirsta į repeating?

## Kodėl aš negaliu keisti atstumų tarp label ir input?

## Kaip padaryti kad flexinamoj zonoj kurioje yra aktyvus marginai top/bot, dedant footeriui background image - isidetu pilnas background image, nes siuo metu deda tik i tarpelius ir nekabina margino top/bot zonos?

![image](https://github.com/user-attachments/assets/eca2a141-d96c-49fd-b1b1-52f7985be379)

## kaip padaryti kad, link'as atsidarytu naujame tab?

## Kaip pridėti link'a prie button tag?

## Kada ir kam naudojamas section ir kuo jis skiriasi nuo div?

## Kaip kurti VSC sablonus?

## Kokia shortcut kombinacija naudojama, jei pvz noriu vienu metu, pakoreguoti visu href elemetu reiksmes?

https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf

## Ar galima parasyti script kad atidarytu dead-server per kitoki browser kuris nera default kompiuterio browser

## Javascript klausimas, ka reiškia "\_\_wm.rw(0);" deklaracija?
