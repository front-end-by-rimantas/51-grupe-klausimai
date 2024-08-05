# 51 grupės klausimai

## ar teisingas būdas skaičiuojant didžiausią skaičių saraše, pradinei dėžutei (JS kode - let max = -Infinity;) panaudoti -Infinity vertę
``js 
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
``
