# 51 grupės klausimai
## Kodėl atsiranda šitas {" "} kaikuriose vietose?
```js
import "./App.css";
import { Header } from "./components/header/Header";
import { Second } from "./components/second_app/second";
import { Counter } from "./components/first_app/First";
import { Footer } from "./components/footer/Footer";
function App() {
  return (
    <>
      <main>
        {" "} <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<ČIA
        <Header></Header>
        <section className="container">
          <Counter name="Zalgiris"></Counter>
          <Counter name="Suodziai"></Counter>
        </section>
        <section className="container">
          {" "}
          <Second></Second>
        </section>
      </main>
      <Footer></Footer>
    </>
  );
}

export default App;
```
## Publishinus puslapy sukurtą su REACT githube kol nepakeitus contento puslapis veikia. Bet kai sudedu savo rašytą kodą deployment nebepavyksta. Gaunu tokią klaidą. Kaip paleisti REACT puslapy githube teisingai?
Annotations
1 error and 1 warning
Build
Process completed with exit code 1.
Build
The following actions use a deprecated Node.js version and will be forced to run on node20: actions/checkout@v3, actions/setup-node@v3. For more info: https://github.blog/changelog/2024-03-07-github-actions-all-actions-will-run-on-node20-instead-of-node16-by-default/
