# ATS

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


console.log( didziausiasSkaiciusSarase( [ 1 ] ) );
console.log( didziausiasSkaiciusSarase( [ 1, 2, 3 ] ) );
console.log( didziausiasSkaiciusSarase( [ -5, 78, 14, 0, 18 ] ) )
console.log( didziausiasSkaiciusSarase( [ 69, 69, 69, 69, 66 ] ) );
console.log( didziausiasSkaiciusSarase( [ -1, -2, -3, -4, -5, -6, -7, -8 ] ) );
console.log( didziausiasSkaiciusSarase( 'pomidoras' ) );
console.log( didziausiasSkaiciusSarase( [] ) );
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
