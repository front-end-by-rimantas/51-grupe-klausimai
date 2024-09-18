# 51 grupės klausimai

## Div'ai overlapina vienas kitą. Gaunasi išsipiešia eilutė ir ant tos eilutės piešiasi visi stulpeliai. Ir gaunasi kiekvienam taške po du div. Any tips, kaip tai išpręsti?

```js
  return (
    <main>
      <TopPanel></TopPanel>
      <SidePanel></SidePanel>
      <div className="container">
        {rowArray.map((row, rowIndex) => (
          <div key={rowIndex} className="block">
            {columnArray.map((row, colIndex) => (
              <div key={colIndex} className="block1"></div>
            ))}
          </div>
        ))}
      </div>
    </main>
  );
}
```
