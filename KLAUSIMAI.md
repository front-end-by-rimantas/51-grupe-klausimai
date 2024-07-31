# 51 grupės klausimai


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

function vidurkis(pasirinkimas){
let tValue = 0;
for (let i=0; i<students.length; i++) { //Ciklas vykdys tiek kartu kiek yra objekte keys ir patikrina visuose keys ar egzistuoja toks studentas
    if (students[i]['name'] === pasirinkimas) { //Jei pasirinktas studento vardas yra objekte
        for (let a=0; a < students[i]['marks'].length; a++) { //Vykdomas sis ciklas tiek kartu kiek parinkto objekto yra key values 
            tValue = tValue + students[i]['marks'][a]; //sumuojama visi pazymiai
        }
        console.log('Studento '+ students[i]['name'] + ' pazymiu vidurkis yra: ' + tValue / students[i]['marks'].length); //Isvedamas atsakymas i console
        } else { 
            console.log('Prasileidau ir katoja students.length viska :/ '); //vistiek isvedamas nors tikiuosi jog isves tik tuo atveju jeigu neatitiks salyga ar yra studentas objekte
        }
}
}
console.log(vidurkis('Maryte'));
```
