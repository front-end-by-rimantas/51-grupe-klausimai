# 51 grupės klausimai

## Kaip reikia užpildyti visus empty items su ta pačia reikšme? pvz "b"
![image](https://github.com/user-attachments/assets/60b0c26a-3a94-4eec-a6d0-4637f24ac596)




## Situacija, turiu du dataContext wrappers. Vienas skirtas handlint loginą, kitas duomenims kurie bus veliau matomi po autentifikacijos. Ar bus teisingas sprendimas duomenų saugumo sumetimais, jog ContextWrapperis kuriame yra sakykime jautri informacija. Negaubs viso puslapio ir bus prieinamas tam elementui tik autorizavus loginą? Ar gaunasi jog pirmu variantu Context wrapper duomenys prades vaikščioti tik po login, o antru variantu jau duomenys butu inicijuojami prieš loginą, ir taip būtų saugumas būtų labiau pažeidžiamas?
https://github.com/JustinasPakalnis/main-project

variantas 1
```js
      <BrowserRouter>
        <LoginWrapper>
          <Header />
          <Routes>
            <Route path="/" element={<Login />} />
            <Route
              path="/main"
              element={
                <ContextWrapper>
                  <ProtectedRoute element={List} />
                </ContextWrapper>
              }
            />
          </Routes>
        </LoginWrapper>
      </BrowserRouter>
```
variantas 2
```js
      <BrowserRouter>
        <LoginWrapper>
         <ContextWrapper>
          <Header />
          <Routes>
            <Route path="/" element={<Login />} />
            <Route
              path="/main"
              element={
                  <ProtectedRoute element={List} />
              }
            />
          </Routes>
        </ContextWrapper>
        </LoginWrapper>
      </BrowserRouter>
```
