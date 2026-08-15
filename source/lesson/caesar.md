# Cezarova šifra

Jedan od velikih vojskovođa koji je koristio šifrirane poruke bio je Julije
Cezar, oko 50. godine prije nove ere. Kada je Cezar slao poruke svojim
generalima, šifrirao ih je tako što je slova u tekstu pomicao za određeni
broj mjesta u abecedi. Primatelji poruke mogli su je dešifrirati jer su znali
vrijednost pomaka — dok su svi ostali vidjeli samo besmisleni tekst.

Na primjer, ako napišete `NIKOLATESLA` i svako slovo pomaknete tri mjesta udesno:

```text
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
```


Slovo `N` postaje `K`, `I` postaje `F` i tako dalje. Dakle, svako slovo
zamjenjuje se drugim slovom koje je za određeni broj pozicija dalje u abecedi.
Kada se dođe do kraja abecede, nastavlja se od početka. Rezultat pomaka za
tri slova udesno je šifrirana poruka `KFHLIXQBPIX`. S druge strane, ako
svako slovo u dobivenoj riječi pomaknete tri slova ulijevo:

```text
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
```


Slovo `K` postaje `N`, `F` postaje `I` i tako dalje. Rezultat tog pomaka
je izvorna dešifrirana poruka `NIKOLATESLA`.

![Cezarova šifra pomak ulijevo](./images/caesar1.png)


## Zadatak za razmišljanje

Razmislite kako biste napravili konzolnu aplikaciju u bilo kojem programskom
jeziku koja će šifrirati i dešifrirati poruke koristeći Cezarovu šifru.
Dani su neki savjeti. Kada ih pročitate, pokušajte napraviti konzolnu
aplikaciju u razvojnom okruženju koje koristite na satovima programiranja.


```{infonote}
Prvi učenik (*vozač*) treba se fokusirati na sintaksu dok piše kod za šifriranje
poruke. Drugi učenik (*navigator*) treba pregledavati svaki redak koda dok se
tipka, tražiti pogreške, postavljati pitanja i predlagati poboljšanja. Nakon toga,
učenici trebaju zamijeniti uloge i nastaviti s pisanjem koda za dešifriranje.
```


Dopuštena abeceda za poruke (i za otvoreni i za šifrirani tekst) može sadržavati
samo mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```


Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni.


U prvom retku korisničkog unosa nalazit će se poruka `m` duljine do sto znakova,
u drugom retku cijeli broj `n` koji predstavlja vrijednost pomaka ($1 \leq n < 26$),
a u trećem retku cijeli broj `s` koji predstavlja smjer šifriranja. Ako je $s=1$,
tada `m` treba biti šifriran, a ako je $s=2$, tada `m` treba biti dešifriran.


### Test primjer 1

Ako je unos:

```text
nikolatesla
3
1
```


izlaz bi trebao biti:

```text
kfhlixqbpix
```


### Test primjer 2

Ako je unos:

```text
kfhlixqbpix
3
2
```


izlaz bi trebao biti:

```text
nikolatesla
```

## Savjeti za rješenje

Budući da engleska abeceda ima 26 slova, pozicija svakog slova može se
predstaviti brojem od 0 do 25.

* a → 0
* b → 1
* c → 2
* ...
* z → 25


Za **šifriranje** slova možete koristiti sljedeću formulu:

```text
nova_pozicija_slova = (trenutna_pozicija_slova + vrijednost_pomaka) mod 26
```


`trenutna_pozicija` predstavlja numeričku vrijednost slova u abecedi,
`vrijednost_pomaka` predstavlja broj pozicija za pomicanje (1–25), a `mod 26`
osigurava da se rezultat vraća na početak abecede ako prelazi `z`.


Za **dešifriranje** slova možete koristiti sljedeću formulu:

```text
nova_pozicija_slova = (trenutna_pozicija_slova - vrijednost_pomaka + 26) mod 26
```


Slično kao kod šifriranja, ali oduzimate vrijednost pomaka, a `+ 26` osigurava
da vrijednost ne postane negativna prije primjene `mod 26`.


## Napredni zadaci s Cezarovom šifrom (opcionalno)

### Proširite dopuštenu abecedu

Napravite konzolnu aplikaciju u bilo kojem programskom jeziku koja će šifrirati
i dešifrirati poruke koristeći Cezarovu šifru. Dopuštena abeceda za poruke (i
za otvoreni i za šifrirani tekst) može sadržavati mala i velika slova engleske
abecede, razmake, brojeve i interpunkcijske znakove!

Aplikacija treba šifrirati ili dešifrirati samo mala i velika slova. Razmaci,
brojevi i interpunkcijski znakovi trebaju ostati nepromijenjeni tijekom
šifriranja ili dešifriranja.

U prvom retku korisničkog unosa nalazit će se poruka `m` duljine do sto znakova,
u drugom retku cijeli broj `n` koji predstavlja pomak ($1 \leq n < 26$), a u
trećem retku cijeli broj `s` koji predstavlja smjer šifriranja. Ako je $s=1$,
tada `m` treba biti šifriran, a ako je $s=2$, tada `m` treba biti dešifriran.


## Koristite funkcije 

Napravite dvije funkcije: jednu za šifriranje poruka i jednu za dešifriranje
poruka. Koristite kreirane funkcije u svom glavnom programu.

Ovdje možete raditi u paru - jedna osoba treba šifrirati poruku, a druga je
dešifrirati!


## Napravite klasu

Napravite klasu `CaesarCipher` koja sadrži:

- konstruktor s parametrom koji prihvaća vrijednost pomaka i osigurava da je
  vrijednost u dopuštenom rasponu,
- privatno svojstvo za pohranu vrijednosti pomaka, s getter i setter metodama,
- javnu metodu za šifriranje poruke,
- javnu metodu za dešifriranje poruke i
- opcionalno, privatnu metodu za obradu poruka koju koriste obje metode.

Koristite kreiranu klasu u svom glavnom programu.


## Prihvatite argumente naredbenog retka

Umjesto čekanja korisničkog unosa, napravite konzolnu aplikaciju koja
prihvaća sljedeće argumente naredbenog retka:

1. argument `m` za poruku,
2. argument `n` za vrijednost pomaka (`0` do `25`), i
3. argument `s` za smjer šifriranja (`1` za šifriranje, `2` za dešifriranje).


## Šifrirajte i dešifrirajte datoteke

Iskoristite dosadašnje znanje za izradu konzolne aplikacije za šifriranje i
dešifriranje tekstualnih datoteka. Vaša aplikacija treba prihvatiti sljedeće
argumente naredbenog retka:

1. argument `m` za naziv datoteke (ili putanju),
2. argument `n` za vrijednost pomaka (`0` do `25`), i
3. argument `s` za smjer šifriranja (`1` za šifriranje, `2` za dešifriranje).
