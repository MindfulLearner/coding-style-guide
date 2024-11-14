# Documentazione by Joshua "Su github @MindfulLearner"

Di seguito a diverse segnalazioni fatte durante la classe, ho deciso di creare questa documentazione per avere una linea guida sul codice che scriviamo.
A mio avviso prima di procedere alla parte struttura del progetto, ne parliamo meglio posso farlo tutto io il setup iniziale per tutti.

## lettura veloce per come fare un commit per bene:
https://www.conventionalcommits.org/en/v1.0.0/
or 
better https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/
TD LR - > per chi non sapesse cosa significa "TROPPO LUNGO DA LEGGERE" lo usero spesso per riassumere :
I Commits Convenzionali sono una convenzione leggera per i messaggi di commit, che facilita la creazione di una cronologia chiara.
"leggere sezione commit in questofile"

# Q&A: 
- Perche' usiamo questa documentazione?
    Perche' cosi' facendo il codice e' piu' leggibile e facile da mantenere. Questo servira' per chi dovra' aiutare o modificare un codice che non e' stato scritto da lui. Anziche' perdere troppo tempo a capire il codice, sapra' guardare e capire il codice in pochi secondi.
- Come facciamo a seguire queste linee guida?
    Semplice, basta leggere la documentazione e seguire le linee guida. Ovviamente io personalmente non dico di seguire al 100% la linea guida ma riuscere almeno ad adattarci almeno per un 50% o 60%. 
- Cosa succede se noi non seguiamo queste linee guida?
    Semplice, faremo un progetto piu' difficile del normale, significa che noi dovremo passare piu' tempo a capire il codice di altri e capire gli errori.
- Cosa ci guadagnate?
    Che a lavoro vi diranno di seguire un modo di scrivere e gia' abituarvi a seguire le regole potra' essere un vantaggio per voi, inoltre se non si riuscira' a completare tutto il progetto perche' pieno di errori, difficilissimi da correggere ci pagheremmo noi. Io comunque "josh" saro' disponibile in caso di domande o aiuti.

# Come procederemo: 
Dato che lavoreremo in Async, potremmo scegliere in gruppo quanti meeting fare. Io propongo di fare 2/3 meeting settimanali, da 1 ora circa ciascuno.
La scelta di fare pochi meeting e' dovuto al fatto che ci divideremo i compiti in file separati ma stessa repository e quindi quando pusheremo e mergeremo.
Ogni volta che andremo ad aggiungere roba nuova faremo feat/nomediquellochefaremo, ovviamente indifferente chi fa cosa quindi non c'e' bisogno di scrivere i vostri i nomi, se ci sara' bisogno di review o particolari osservazioni verra' chiesto sul gruppo

---
## DA NON LEGGERE QUESTA PARTE
Ognuno che avra un ruolo aprira un branch esempio "feat/nomediquellochefarete". Dopo aver terminato il proprio compito, aprire un pull request solo quando avete terminato il compito "molto semplice" e poi fate il merge.
Esempio: 
  1. "josh" apre un branch "feat/FrontEndHeader"
  2. "josh" termina il compito e apre un PR (pull request) apparira' in automatico su github il bottone per aprirlo
  3. Se non ci sono problemi allora josh chiude il PR e poi fa il merge e' un bottone unico lo vedrete li subito.
- Perche' fare questo anziche pushare e mergiare e basta?
    Perche' cosi' facendo noi possiamo controllare il codice di ogni membro del gruppo e possiamo fare subito commenti sul codice e quindi evitare errori e problemi che potrebbero essere fatti.
---


# Come procederanno gli aiuti? IMPORTANTISSIMO NON HO VOGLIA DI SPIEGARE TRAMITE DISCORD O CHIAMATA COSA FARE.
Quando un membro del gruppo chiede una mano aprira una Issue in cui spieghera' il problema e cosa ha fatto finora.
Quello che faranno quelli che vorranno correggerlo, vedranno la Issue, commenteranno cosa non va. 
- Se proprio c'e' bisogno di aiuto andremo sul codice sistemiamo il codice e poi mi occupero a fare il pull request 
- quello che dovra fare quella persona e' aspettare la correzione nel mentre lavora su altro e poi solo git pull.


Ora detto questo, passiamo al succo documentazione.

---
# Guida di Stile del Codice by Joshua "Su github @MinfulLearner"

Importante: PUSHATE MOLTO PIU' FREQUENTEMENTE. Ovviamente se cambaite una riga e basta non serve. Ma non voglio vedere 1 commit ogni 2000 righe scritte. Questo e' importantissimo cosi se devo leggere i commit prima dell'errore non ci metto piu' di 10 secondi a capire cosa e' stato fatto o il problema.

## Convenzioni di Nomenclatura
- **Variabili**: Utilizzare il `camelCase` per le variabili, iniziando con una lettera minuscola e capitalizzando le parole successive. Ad esempio: nomeUtente, contatoreElementi.
- **Funzioni/Metodi**: Seguire il `camelCase`, iniziando con un verbo che descriva l'azione svolta. Ad esempio: slugGenerator(), postUserInfo().
- **Classi/Moduli**: Adottare il `PascalCase`, iniziando ogni parola con una lettera maiuscola. Ad esempio: ProductController.php, ProductSeeder.php

- **Encoding**: EVITATE ROBE DEL TIPO `itemList` questa pratica si chiama encoding. Quindi `itemList` diventera' `items`.
```php
$itemList = [];
```
diventera'
```php
$items = [];
```

- **Expand Abbreviations**: Quindi esempio: `f` diventera' `funzione` evitate codici come `f` o `c` o `sub` o `func`... etc..
```php
function f() {
    // codice
}
``` 
diventera'
```php
function funzione() {
    // codice
}
```

- **usate distinzioni pulite**: Esempio: `calcolo` diventera' `calcoloPrezzo` o `calcoloTotale` etc...
```php
function calcolo() {
    // codice
}
```
diventera'
```php
function calcoloPrezzo() {
    // codice
}
```

- **magic value**: Quindi esempio di codice:
```php
$prezzo = 20 + 10;
// ritornera' 30
```
diventera'
```php
$prezzo = 20;
$prezzo = $prezzo + 10;
// ritornera' 30
```

## Formattazione del Codice 
Questa parte e' un po indifferente perche' non ho voglia di impostarvi prettier in modo che sia tutto uguale. In caso lo impostero io sul progetto.
- **Indentazione**: Indentate sempre. basta che sia leggibile.
- **Lunghezza delle Linee**: indifferente basta che sia leggibile.
- **Spaziatura**: indifferente basta che sia leggibile. 

## Struttura del Codice In caso doveste creare roba nuova
- **Organizzazione dei File**: Esempio: questo solo se riuscite, io normalmente riesco a capire comunque cosa scrivere se scrivete bene i nomi.
```css
src/
├── HeaderComponents/
│   ├── components/ /* ovviamente solo se e' necessario ovviamente fare Header e basta con tutto senza componenti si puo fare i ncaso voleste farlo pulito */
│   │   ├── Logo.vue
│   │   ├── Navigation.vue
│   │   └── SearchBar.vue
│   └── Header.vue
│
├── MainComponents/
│   ├── components/
│   │   ├── Content.vue
│   │   ├── Sidebar.vue
│   │   └── Article.vue
│   └── Main.vue
│
└── FooterComponents/
    ├── components/
    │   ├── FooterLinks.vue
    │   ├── Copyright.vue
    │   └── SocialMedia.vue
    └── Footer.vue
```

- **Ordine degli Elementi**: Le funzioni SEMPRE SOTTO SEMPRE SOTTO!!! mentre in Vue ovviaemnte nei methods
```php
class TypeController extends Controller
{
    /**
     * Display a listing of the resource.
     */
    public function index()
    {
      createSlug();
    }
/**
 * questo e' messo sotto SEMPRE SOTTO!!!
 */
   public static function createSlug(
    {
      // esempio
    }
}
```

## Documentazione e Commenti
- **Commenti in Linea**: usare // <!-- --> etc...
- **Commenti di Blocco**: MA PER BLOCCHI DI CODICE USARE javadoc https://jsdoc.app/about-getting-started
esempio: 
```php
/**
 * questo e' un commento di blocco SWAG
 */
function esempioFunzione() {
    // codice
}
```
a cosa serve?
che se io metto sopra il mouse ovunque io uso esempioFunzione() leggero "questo e' un commento di blocco SWAG"

- **Documentazione delle Funzioni**: 

## Gestione delle Versioni
- **Commit**: come detto gia sopra commitare spesso solo si ha scritto il necessario. non pushate una riga di codice
- **Branching**: come detto sopra usate feat/nomediquellochefarete.. mentre io per correggere codice userei un altro branch tipo fix/nomedelbugenomedelvostro
- **Gestione degli Errori**: Documentazione + chiedere aiuto, prima ovviamente provateci da soli guardate anche i video o slide vecchi
## Glossario commit
- fix: per correggere un bug.
- feat: per aggiungere una nuova funzionalità lo usero per creare componenti, sezioni e tutto.
- BREAKING CHANGE: indica un cambiamento rilevante nell'API.
- Sono ammessi altri tipi come build:, chore:, docs:, style:, refactor:, perf:, test: ecc. // se interessati a usarlo cercare su internet!
## vantaggi commit: 
- Comunicazione chiara delle modifiche.

## Strumenti e Configurazioni
- **Editor/IDE**: Utilizziamo tutti vscode
- **Linting e Formattazione**: Non ne useremo perche e' da impostare.

finito
