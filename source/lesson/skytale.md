# Skital

Nakon završetka ove lekcije, moći ćete:

* Objasniti kako funkcionira Skital šifra.
* Implementirati šifriranje i dešifriranje koristeći jednostavne operacije s poljima ili nizovima znakova.
* Razumjeti kako se fizički uređaji za šifriranje mogu digitalno modelirati.

Skital je jedan od najstarijih poznatih alata za šifriranje, koji datira iz
antičke Grčke oko 400. p.n.e. Bio je to jednostavan cilindrični uređaj koji su
Spartanci koristili za slanje tajnih poruka tijekom vojnih pohoda.

Traka pergamenta ili kože omotavala se oko drvenog štapa (*skitala*)
određenog promjera. Poruka se zatim pisala duž štapa. Nakon odmotavanja,
slova su izgledala razbacano i besmisleno. Primatelj je trebao štap
**točno istog promjera** kako bi omotao traku i pročitao originalnu poruku.

Ako želite šifrirati poruku:

```text
attackatdawn
```

i odaberete štap koji omogućuje **4 slova po okretaju**, najprije pišete
poruku vertikalno u stupcima, formirajući retke duljine 4:

```text
a t t a
c k a t
d a w n
```

Šifrirani tekst se zatim formira čitanjem redak po redak:

```text
acdtkatawatn
```

Za dešifriranje, primatelj ponovo omota traku oko štapa istog promjera
i čita vertikalno kako bi rekonstruirao originalnu poruku.

## Prvi zadatak

Napravi konzolnu aplikaciju u bilo kojem programskom jeziku koja će šifrirati i
dešifrirati poruke koristeći Skital šifru. Koristi razvojno okruženje koje
koristite na satovima programiranja.

Dopuštena abeceda za poruke uključuje samo mala slova engleske abecede:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```

Razmaci, velika slova, brojevi i drugi znakovi nisu dopušteni!

U prvom retku korisničkog unosa bit će poruka `m` duljine do sto znakova. U
drugom retku bit će cijeli broj `k` (broj stupaca – opseg štapa). U trećem
retku bit će cijeli broj `s`, koji predstavlja operaciju. Ako je $s=1$, tada `m`
treba biti šifrirano. Ako je $s=2$, tada `m` treba biti dešifrirano.

### Test primjer 1

Ako je unos:

```text
attackatdawn
4
1
```

izlaz bi trebao biti:

```text
acdtkatawatn
```

### Test primjer 2

Ako je unos:

```text
acdtkatawatn
4
2
```

izlaz bi trebao biti:

```text
attackatdawn
```

## Savjeti za rješenje

Za **šifriranje**, zapišite otvoreni tekst vertikalno u tablicu s `k` stupcima.
Čitajte tablicu redak po redak kako biste formirali šifrirani tekst. Za
**dešifriranje**, zapišite šifrirani tekst redak po redak u tablicu s `k`
stupcima, čitajte tablicu vertikalno kako biste rekonstruirali otvoreni tekst.

## Složeniji zadaci sa Skital šifrom (opcionalno)

### Proširite dopuštenu abecedu

Uključite velika slova, razmake, brojeve i interpunkciju.

### Koristite funkcije

Napravite funkcije `encrypt()` i `decrypt()` kako bi kod bio modularan.

### Napravite klasu

Implementirajte klasu `SkytaleCipher` koja pohranjuje `k` i pruža metode za
šifriranje i dešifriranje.

### Šifrirajte i dešifrirajte datoteke

Izmijenite program tako da čita otvoreni tekst ili šifrirani tekst iz datoteke
i zapisuje rezultate u drugu datoteku.

### Rukujte nepotpunim recima

Izmijenite program tako da, ako je posljednji redak kraći od `k`, ispravno
šifrira i dešifrira rukujući nedostajućim znakovima ili dopunjavanjem.
