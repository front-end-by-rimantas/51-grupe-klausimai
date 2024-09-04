# 51 grupės klausimai

## Ar galima paleisti github pages iš nepagrindinio branch?

## Kodėl Uždėjus evenListener ant playBtn, nebeveikia window eventListener? [project](https://github.com/ZydrunasK/block-adventure/tree/menu)
```js
const gameDOM = document.querySelector('.game');
const playBtnDOM = document.querySelector('.playBtn')

playBtnDOM.addEventListener('click', () => {
    gameDOM.innerHTML = `<div class="line">${'<div class="sqr"></div>'.repeat(15)}
    </div>`.repeat(15) + '<div class="blockMan"></div>';   
})

const lineDOM = document.querySelector('.line');
const sqrDOM = document.querySelector('.sqr');
const blockManDOM = document.querySelector('.blockMan');

const sqrSize = 48;

const blockManPos = {
    x: -14,
    y: -6,
};

window.addEventListener('keydown', event => {
    if (event.key === 'w') {
        if (blockManPos.y > -7) {
            blockManPos.y--
        }
    }
    if (event.key === 's') {
        if (blockManPos.y < 7) {
            blockManPos.y++
        }
    }
    if (event.key === 'a') {
        if (blockManPos.x > -15) {
            blockManPos.x--
        }
    }
    if (event.key === 'd') {
        if (blockManPos.x < -1) {
            blockManPos.x++
        }
    }
    
    blockManDOM.style.top = (sqrSize * blockManPos.y) + 'px';
    blockManDOM.style.left = (sqrSize * blockManPos.x) + 'px';
    console.log(blockManPos.x, blockManPos.y);
})****
```
