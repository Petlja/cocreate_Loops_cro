# Cezarova šifra

Jedan od velikih vojskovođa koji je upotrebljavao šifrirane poruke bio je Julije Cezar, oko 50. godine pr. Kr. Za zaštitu vojnih komunikacija koristio je jednostavnu šifru poznatu kao Cezarova šifra. Ova se šifra naziva i šifra pomaka jer se svako slovo otvorenog teksta zamjenjuje slovom koje se nalazi određen broj mjesta ispred ili iza njega u abecedi.

Primjerice, ako napišete `NIKOLATESLA` i svako slovo pomaknete za tri mjesta ulijevo:

![Caesar Cipher Left Shift](./images/caesar1.png)

```text
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
```

Slovo `N` postaje `K`, `I` postaje `F` itd. Dakle, svako slovo zamjenjuje se drugim slovom koje je u abecedi udaljeno za određeni broj mjesta.

**Dešifriranje** radi na isti način, ali obrnuto. Da biste dešifrirali šifrirani tekst, pomaknite svako slovo za tri mjesta natrag udesno:

```text
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
```

Slovo `K` postaje `N`, `F` postaje `I` itd. Rezultat ovog pomaka izvorna je dešifrirana poruka `NIKOLATESLA`.


## Zadatak za razmišljanje

Razmislite kako biste u bilo kojem programskom jeziku napravili konzolnu aplikaciju koja šifrira i dešifrira poruke pomoću Cezarove šifre.

```{infonote}
Prvi učenik (*vozač*) treba se pri tipkanju koda za šifriranje poruke usredotočiti na sintaksu. Drugi učenik (*navigator*) treba pratiti kod, predlagati poboljšanja i postavljati pitanja. Nakon šifriranja zamijenite uloge za dešifriranje.
```

Dopuštena abeceda za poruke (i za otvoreni i za šifrirani tekst) može sadržavati samo mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```

Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni.

U prvom retku ulaza nalazi se poruka `m` koja ima najviše sto znakova, u drugom retku cijeli broj `n` koji predstavlja vrijednost pomaka (1–25), a u trećem retku cijeli broj `s` koji predstavlja smjer šifriranja. Ako je `s=1`, `m` se treba šifrirati, a ako je `s=2`, `m` se treba dešifrirati.

### Primjer provjere 1

Ako je ulaz:

```text
nikolatesla
3
1
```

treba biti izlaz:

```text
kfhlixqbpix
```

### Primjer provjere 2

Ako je ulaz:

```text
kfhlixqbpix
3
2
```

treba biti izlaz:

```text
nikolatesla
```

## Savjeti za rješenje

Budući da engleska abeceda ima 26 slova, položaj svakog slova može se prikazati brojem od 0 do 25.

* a → 0
* b → 1
* c → 2
* ...
* z → 25

Za **šifriranje** slova možete koristiti sljedeću formulu:

```text
new_letter_position = (current_letter_position - shift_value + 26) mod 26
```

`current_letter_position` predstavlja numeričku vrijednost slova u abecedi, `shift_value` predstavlja broj mjesta pomaka (1–25), `+ 26` osigurava da vrijednost ne postane negativna, a `mod 26` osigurava vraćanje na početak abecede.

Za **dešifriranje** slova možete koristiti sljedeću formulu:

```text
new_letter_position = (current_letter_position + shift_value) mod 26
```

Na isti način kao i pri šifriranju, ali se vrijednost pomaka zbraja, pa vrijednost ne može postati negativna i `+ 26` nije potrebno.

## Složeniji zadaci sa Cezarovom šifrom (izborno)

### Proširite dopuštenu abecedu

Napravite konzolnu aplikaciju u bilo kojem programskom jeziku koja šifrira i dešifrira poruke pomoću Cezarove šifre, ali s proširenom abecedom.

Aplikacija treba šifrirati ili dešifrirati samo mala i velika slova. Razmaci, brojevi i interpunkcijski znakovi trebaju ostati nepromijenjeni.

U prvom retku ulaza nalazi se poruka `m` koja ima najviše sto znakova, u drugom retku cijeli broj `n` (vrijednost pomaka od 1–25), a u trećem retku cijeli broj `s` (1 za šifriranje, 2 za dešifriranje).

## Upotrijebite funkcije 

Napravite dvije funkcije: jednu za šifriranje poruka i jednu za dešifriranje poruka. Upotrijebite izrađene funkcije u glavnom programu.

Ovdje možete raditi u paru – jedna osoba treba šifrirati poruku, a druga je dešifrirati!

## Izradite klasu

Izradite klasu `CaesarCipher` koja sadrži:

- konstruktor s parametrom koji prihvaća vrijednost pomaka i osigurava da je vrijednost u dopuštenom rasponu (0–25),
- privatno svojstvo za spremanje vrijednosti pomaka, s getter i setter metodama,
- javnu metodu za šifriranje poruke,
- javnu metodu za dešifriranje poruke i
- izborno, privatnu metodu za obradu poruka koju koriste obje metode.

Upotrijebite izrađenu klasu u glavnom programu.

## Prihvatite argumente naredbenog retka

Umjesto čekanja na korisnički unos, napravite konzolnu aplikaciju koja prihvaća sljedeće argumente naredbenog retka:

1. argument `m` za poruku,
2. argument `n` za vrijednost pomaka (`0` do `25`) i
3. argument `s` za smjer šifriranja (`1` za šifriranje, `2` za dešifriranje).

## Šifrirajte i dešifrirajte datoteke

Upotrijebite dosad stečeno znanje za izradu konzolne aplikacije koja šifrira i dešifrira tekstne datoteke pomoću Cezarove šifre.

Aplikacija treba prihvatiti sljedeće argumente naredbenog retka:

1. argument `m` za naziv datoteke (ili putanju),
2. argument `n` za vrijednost pomaka (`0` do `25`) i
3. argument `s` za smjer šifriranja (`1` za šifriranje, `2` za dešifriranje).
